# Simple Batch Obfuscator

**Disclaimer: This project is for educational purposes only!!!**

This program creates an obfuscated batch script that executes a command.

### TODO

- encrypt and decrypt payload at runtime using base64 or AES
- create CLI
- write tests
- add more configuration options

before:

```shell
$Ca=".,-~:;=!*#$@";$sin=@(for($i=0;$i-lt 1000;$i+=1){[Math]::Sin($i*0.006283185307179)});$cos=@(for($i=0;$i-lt 1000;$i+=1){[Math]::Cos($i*0.006283185307179)});$isUnix=([System.Environment]::OSVersion).Platform-like'Unix';$hasResize=@(get-command resize).Count-gt0;if($isUnix-and$hasResize){[void](resize -s 44 80)}else{[void][System.Console]::SetWindowSize(80,44)};Clear-Host;while($true){$oA=(' '*3520).ToCharArray();$dA=[double[]]::new(3520);$tsA=$sin[($aA%6.28*159.15)];$tcA=$cos[($aA%6.28*159.15)];$tcB=$sin[($aA%6.28*159.15)];$tsB=$cos[($aA%6.28*159.15)];$aY=0;while($aY-lt6.28){$tcY=$cos[($aY%6.28*159.15)];$tsY=$sin[($aY%6.28*159.15)];$tscYA=$tsY*$tcA;$Dp=$tcY+2;$aX=0;while($aX-lt6.28){$tcX=$cos[($aX%6.28*159.15)];$tsX=$sin[($aX%6.28*159.15)];$tscXY=$tsX*$tcY;$iD=1/($tsX*$Dp*$tsA+$tscYA+5);$tp=($tsX*$Dp*$tcA-$tsY*$tsA);$sX=[int](40+40*$iD*($tcX*$Dp*$tcB-$tp*$tsB));$sY=[int](20+20*$iD*($tcX*$Dp*$tsB+$tp*$tcB));$Ix=(8*(($tsY*$tsA-$tscXY*$tcA)*$tcB-$tscXY*$tsA-$tscYA-$tcX*$tcY*$tsB));$idx=$sX+80*$sY;if($dA[$idx]-lt$iD){$dA[$idx]=$iD;$oA[$idx]=$Ca[$Ix]};$aX+=0.02};$aY+=0.07};$aA+=0.09;[Console]::SetCursorPosition(0,0);[console]::write([string]::join("",$oA))}
```

after:

```shell
@echo off
%RoGLDYDoGkgKSPqpvjFlSINEpbYNzVwr%s%DqNcVNwSlsHWkhsOrJtaNZJPeTADlaTQ%%AzOuMkkGoOvUVkzAkYUaMDnZBKrLZbPC%e%qBVrGjljKpxNRZkQUXMwUUPjnOwDPXbc%%QKNLCRqFARcLLLRbEPHqQZODWmimffwH%t%rWAUgAlYRnfwBRwyLkLnFDtjRuHuklwj%%oSfpBYuyKRYheZLRYBJrwFffHIeeabBL%l%qIhFBbWzwPiWYjdhzCKmXeIiMulGpXtm%%nWHxxDbGzjziVtYrjfKbmbqDTjRzucwP%o%WWxlCKMYdpSEaHixHUunxDOOxglMnNyK%%AyeFIAAJWoBfBAoPiPCednFnFtuFdvge%c%JQyMPvXaxCGtOOdrxUefKIgLeqUMHEXc%%bmOiXGdsJNskXkzHUYnvinKMLYjRlytD%a%aqkxVOvVvyCkEgAEOPULnkgoIZChtLTm%%eYGrdnkrHcVZZMewjzrYxudepZlZlmAV%l%yGXPhrwAfDcyYZoesrMnYfQbmDhFOJZy%%JKvgkuBkgzGaZAGyGCIjsBwbwTKnoBMN% %WglhdPLezEmwPVdbABSgpsUGJGzosbjQ%%SqcJgkSfUGGWGIHIGyqfEcrvruDJoYxG%e%VrfDuQqorwOUOirFJqvXKRiJyFGOQpPi%%yhFxOKtKruEeJUIpNatkliDaXSEhoFPD%n%eAVXotbivZkmPdaanIdxsqKhkBRHuAUG%%bvJBDrnEOLaqhltEBThlZZdkpeluwVDh%a%WCCzUaitCIhczVGkjSIVFvdcfuSYJkvk%%QnLPQjkOKhXAWAezIYWQnEjtoAaqFFyO%b%afiuIpzKJNmsvbrFgXWfCwjtTCTPTcYs%%RmHuKYcWGgKiOsvYeHVQfQQyvFAGbfXk%l%kOXkKLDeNwTZYilLsZMqTDwiJFfKORxo%%mEzTWtDFeiTOEwOhDrQsGnUlAZiSemTF%e%IPSieiRwberwHbspvDtxKmLwBhDgIyhX%%eOLKkPflUAQWuqZahShzOFFXDVipcuak%d%RqSiLlMxRTuVJVjpMxajdMIZjkYRRAgf%%mjRnvthFkjmFwangXgBeWcsklnZqxicH%e%ahaaEtlOPnLvowheCTqvyXFYaStkSGWm%%DaBwJkrerzadwuaKlZECSFRUlpnvZidm%l%nICCBkKvDbwnkxPreeUoPxHeSBxFhXLq%%fQIENXszJWisnVDsaOhaPpEXzQxfvKxR%a%kMvypmgUDjintoRqNWVUeXVOPqfUHaEy%%EOucpMcBoOgBsRukJzemctcAnqujeGpG%y%qhasIckQGdwDJzDsInzFMtLZNExIKYKa%%lyqdMcOIHyrckzWTkKbENjzOEOItFgAW%e%prgmFuJnPOvXZkgMcDtnWOKQMwzafbzh%%bMgyipxJzDTXFNCwlxyxtvQuVRGmEGae%d%XxlcTHBdYIdlTaCFYXiyTxptVQxMfzDM%%aObIUYqfiAEcmLhnSqLVahrXfvZkcCgk%e%zAnQhuZRwZbSKmGKbgXNHDMVCahfvWLJ%%GotheSQAijYROwwBWYOECJanLUKjJUlC%x%xQSuDsukRhSteORWSRejSrbvleghsCEl%%NkhZfvKbXJaZAhXwkuCPVtoGachkNPvO%p%REyufEKMjhFbXtuZGuZHRdKSFwbpquHR%%aBWpmfOmZXvgENNDpYejVRFBFWupDHrb%a%YJOkfhCeUWsoPVOOqGTSKtDCOABWDZGp%%bvyvjkiwWqQgrXZlgJNavxuHnfMAGHGw%n%sVUEjkboxKvvhpxXKyALkGVPfpQeviDW%%lcLWZXnehAbAERHuyTKZeyKYcNIRsycc%s%jKFKVbQFHqXEUOpYrPMkjkzoXoGxMAsP%%meXsUQMAwDGuUMmRIIloSIkNsxbUUAbK%i%PsRNBhgJlcNtIVgUEAjiJvEEgaCgpvTB%%LkVpuVoeqiRhnVKESqMWdhAmAHlPwtnw%o%jupMwiPDfgWOcSwCIvdQXzedBKwQmARE%%mkJiqgXWnzhOQWLSYVsEqfhnLfQcCBZR%n%kaVsMnDGvlCcBtLDdBrOIwRSsZruLBTh%
set "OCLIEZDtxdGZcoWpDDsaFeUIjnIbrqrb=s"
set "BNNOzLcsDOyomOXkvTeeLqdOIDBvqFto=t"
set "goMzBiWYAvJaKWYzsCQybYPAgeLbSihV=!OCLIEZDtxdGZcoWpDDsaFeUIjnIbrqrb!e!BNNOzLcsDOyomOXkvTeeLqdOIDBvqFto!"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "vJYyKAkppkrSUFKOPojnhInjWvyUNloG=QBsAHQAJABpAEQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "GdOBcywxUNEHhnDvcZAAShNCwtrIdSsZ=YAD0AJABjAG8Acw"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "zoPVtOMmmEnhuXtBapsLGUmEggDDgtUi=kAHQAcgB1AGUAKQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jswCBpKVgXcoKEAgWMguzXkKkzShQdgJ=HQAcAAqACQAdABz"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "EtVeFpgjxzLWMkQIkYTMXfyrAyEhDNMo=DIAOAAqADEANQA5"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "CEQMPgYqlQxWxtiRdHExpELpNyceoqlv=-EncodedCommand"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hfxbBziXZTOUaMkmmFtaXEdFjAnHgQaO=wA1ADIAMAApADsA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "CJmbLKYSpSHaVvAIuyTKuvqNElKICJST=AGMAWABZACoAJAB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jlIfqnzaijSQSqZgBkuwdPGaRpVaBSOb=FMAVgBlAHIAcwBp"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ZekWFDOMmhMPlBqRMUjvUDXUuVmJfLYB=AMgA4ACoAMQA1AD"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "mJsTvjOmhCuHUZStoYtwxaSKAcpJamRT=ACQAcwBZADsAaQB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kvQdbfQQbCnjvidcKGqeQOPlbnPHtEvR=QgA9ACQAYwBvAHM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "rkwJRmooqgDqJFkMOOgrZksAvLrCUowb=QAnAFUAbgBpAHgA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ToqxmNWSbEKXYwTvINOVReKKlrXTPGqK=HQAaABdADoAOgBT"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "mqcuvQXOncXQjGoCcOSnLyYZOFbnetnI=BuAGkAeAA9ACgAW"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "DTZRcqBGYKXfDEZLmzDJYpxSeSZfcpuA=CQAdABzAFgAKgAk"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "uVuQqHKduINTSHcvZDZGwIHMbrTyuViN=AKQB9AA=="
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "DisqpJBGBnHuxeKjsLqZAfBexpjYjULQ=AGMAQgApACkAOwA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "liGWHfIyrVLwBEIwCOiYyPRiqGDdbyox=AAtAHMAIAA0ADQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "QhPcvIJHDFyHBFcMQviAXIpkGmVncGKg=egBlACgAOAAwACw"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "OOchLjtCSWQTGfEqeckusbWVNElxNNBG=vAGwAZQBdADoAOg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "juArooPrSdQtBTrZjJvpfxPDHXfJSYIm=AHcAcgBpAHQAZQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "KDvsZeOebWuOoESvFtyGqmAFdkycfhSr=A7ACQARABwAD0AJ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "zsrSJGmSJnyHokBtHeFgsIKrxXUExBai=UANgAuADIAOAAqA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LbSFrrIlqizStWtSCEWjhMdmQSBeyDLU=ZACoAJAB0AGMAQQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YKCNVtmHWjqXwgLEMSSgfctMWANymuls=wBZACoAJAB0AHMA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "FZfjncfWBkxIjcTOXMXoGCeQUxAhpqMX=oAFsAcwB0AHIAaQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "WTTZBzBmsmAaZFqacGySDiNYNGylcCTy=D0AIQAqACMAJABA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "SfvwzzERAepjpyGMFHUNKrROqssnPuNm=AVQBuAGkAeAAtAG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "BOTqHlmSybXEmMephXiFVlJKRUTzXHmg=AkAGkAZAB4AF0AL"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "MKUuLXYcUksyDzwSFAINQuWOpDmfQQBU=mACgAJABkAEEAWw"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "BAQLsAMjcAsfCyDIVmMTcopZVILYFYSX=QAdABjAEIALQAkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "SqeWuHZDDCjQkfKHEyOPqQYaxxAqFfKg=AAMAA2ADIAOAAzA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kzkNIUTsmcyUECtdkEmWIudjTaDSmmIa=AC4AMQA1ACkAXQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "fSpnCzemWQljcMezqUQPjzwVbTLqelSW=AGgAaQBsAGUAKAA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "stWFhDhIxyTBqcKJmslzJobJghbSgidc=dABjAFkAKgAkAHQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "XepkkVqYvTtgdFENPhzcJWYCpcLoaqit=HQALQBjAG8AbQBt"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hkPfdmeOzmSoKUlfKZRMdBPsmnTFtFIG=KQB7ACQAZABBAFs"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YUqXMkwPwQFUcNTkoeQaanjOfbbOutBp=sAWwBjAG8AbgBzA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jfIuNshxMRUEtJIVVKInMlCXZOiywmQc=AKgAkAEQAcAAqAC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "wmujLTvoHNsZXfzIKHgjlgBTKkseGYAm=AC0AbAB0ACAAMQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "rINfcbMjKAxjURqPPWkqpoSTEHAxKarK=YAbwBpAGQAXQBbA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "wIaGQfGdGRDhDlraSbCuXcmZLLHpuGLW=AGEAbgBkACAAcgB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "EkvWOoMrCYjdyOUTsVeaUMpCDrLJhYll=wADAAMAA7ACQAaQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "OisiVKqrEwDsENvzFHUOcjxBVukowIZV=CQAdABwACoAJAB0"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ZgOwNCysxFAImHbFxbdOzmOPkHnzigAV=APQAwAC4AMAA3AH"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ptaipqfUzgRBDAbaaRzHpjvAtCZtYrNy=dAAgADEAMAAwADA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "TpdJIGdxYfXInfrEXiTgSWEDRkILnwAw=DEANQA5AC4AMQA1"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "HPzXLBGfRiefAGnRgxpQfXuOXAeScgZH=AHgAXQA9ACQAQwB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "yTqIOVRqNAAMQDvDGTXLQpKevUwoVOLp=AEIAKQApADsAJAB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "NgZCJWBeVjPKRQGtswEGJatjgnpzjgWk=QBZAC0AbAB0ADYA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YHCTMKZWGLUyWcuqKoVzlzUVHgcxnEpH=cwBpAHQAaQBvAG4"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "vxPYQLoxBpHEsVdnWeiTxfVYzYCzUdJO=AB0AGMAWAAqACQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "RFiXVFEzPnjiElmrmfkRbKcBhZcmDbmb=AFsAQwBvAG4AcwB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "QVYlBQUOpMRSdlQRadVYGDNyzGdKgVCd=AGkAbgAoACQAaQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "REMLtrqsINbvWvnIuECkKbOzTGBenqZG=D0AJABzAGkAbgBb"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "SXRgnlxHwZQFcUbJjQQTXxcoGhZWZDBH=ACkAewAkAHQAYwB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "lwKHmWMAemXrTFXsgSVDbHhhvuoMPbFg=kALgAxADUAKQBdA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hwFhwJaxXXdwurvhjKTtBiyEGJzzsknX=ACgAJABhAEEAJQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "oHPhevdnirNKRiTIWCDXxGAqqRfMbvJn=EAKQB7AFsATQBhA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "HYQPWJzyNfiBzLrZRFxziQlXFyizLYDh=IgAsACQAbwBBACk"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "XKNepqGxWuXWAneqLZBfpNpeMaPMiEPW=AEQAcAAqACQAdAB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "eeqXaNZTFaroLDIZzdsBwkmHOIJjhshD=gBkAG8AdwBTAGkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YgMdTeeJklQMgWrqSJcZhOrqzinJZgcs=AKAAwACwAMAApAD"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "QwFMjLnlQEwKCPCMAeQKLjAYLcLDGTLq=BbACgAJABhAFgAJ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "gJmLmphKnpetZFMauKXywqlBTCsaTADc=OwAkAGEAWAA9ADA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "JOglywWAIIsXCqGEZzUHtBOjkILITPTA=GMAQgAtACQAdABz"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kLMmjMcAFmaEOhAoaFlmcMglZmWogxjW=B7ACQAbwBBAD0AK"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "XWmBIDMOINqEFufJgfAFAhTWhkDjuFhp=AB0AGMAWQArADIA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ycsjwqPScCTZmZYRuwUbdabuFUUobHkb=HMAWQAqACQAdABz"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "fZjxnFMQbToFTXDlyrHihFeADhsbcrjq=CkAOwAkAGQAQQA9"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "IMSTJemmkhVkPoZYPKgqYJzjfMujNwnW=zAFkAPQBbAGkAbg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "UZJJmpuaOhJarhzMsJJbslRfNgGWbcrj=AkAHQAcwBZAD0AJ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "yzERozVHUASWEpSiSvfaoPsWBNnrZZfo=bQAuAEUAbgB2AGk"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "sTgSpkZNpfMwsQZKwxRhxbqBPSqzDerL=AJABpAGQAeABdAD"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "fKFYUGzJFsyCsmrHbbkviDKjwdZczXVw=kAEkAeAA9ACgAOA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "BdVOuSXgXiCeCtefzDtMEppxIyxPWIrK=AkAGMAbwBzAFsAK"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LEFcUeBTsDGSrPjCFtfNrCLXaCdmtFvK=gAZgBvAHIAKAAkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "cycScIVrKpjzpRGeEUNoVdsdoCmithqQ=FMAeQBzAHQAZQBt"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "BGJbJEmvqWXlhEmnMaXOUtXWXwxOQzen=ArAD0AMQApAHsAW"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "OErjrJJJBZgZWibHDnODruTqexbqRNYD=2AC4AMgA4ACoAMQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "DlfMpbbeCJJcQPwvkvdHmAQpSkaRYThd=zAEEAKwAkAHQAcw"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "WxtnaIOxXarzDBUHVtoGwgzRLaKnKPAT=hAFsAJABJAHgAXQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "sylTwayROvSFYsBcxNRbPwSkBRbtfuOY=AEEAPQAkAHQAcwB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YtRObiLwsePyLxOMHKKNGQoTqOWOuPss=AFsAZABvAHUAYgB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "KOtoZJlKPfZyJNNWdeKhxZLujrwGuYlr=G4AWwAoACQAYQBY"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "mjubFPCGjKvuVBezPzSLKgPiMkiLHCdC=JwA7ACQAaABhAHM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "lfQVtlqXUBKQhqxykWXUowHxNQLFAwWj=AdABjAFkAOwAkAG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YPrykEGvigaqHWulohvKVTCDSKYQlykv=BzAGMAWQBBAC0AJ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jqSJKOiGCInmfGKbWlvBIUuOfDDAymTY=NQAyADAAKQAuAFQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hnFLnLggClXqYcdrNJDeJKmckpJwwnOj=MAbwBzAFsAKAAkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "brGSmTGfxzlgdHPsbLnwyflefhAmOgCQ=QAzADAANwAxADcA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "KAmgANemAlJpcDDjSjiBHHQOISGMnSdc=IAA4ADAAKQB9AGU"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "pNOhLHBPnAsxIAGRyWyPVsYRDknXkkKc=BjAFkAQQArADUAK"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "slhijcLafreHgjmZMyKvBfQFkEdihJWF=7ACQAdABjAEEAPQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ljAagDUzzHoRQgRPqcvFLlgcRTHOKJXB=wBNAGEAdABoAF0A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "pPURVMhdoeeBVAVPsSwBlGoBvzGKLlCZ=wBTAHkAcwB0AGUA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "tYVHRnVTOXjGjozaoCuLXwfPssunnXsz=JAB0AHMAQQA9ACQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ixiedIlDwYMVOrKwrVXvPoQCEYFMovhS=DsAJAB0AHMAYwBZ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kEsDHxRPdKtbCQywAFGgTGehyDuboOJF=A1ADkALgAxADUAK"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "STWQdRclSfbmBAQTetBNxIMqkcEhGDTN=AA7ACQAaQAtAGwA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "HaEBevbEDivBppnoSCvoCiXkggxNqnXK=gBvAGkAbgAoACIA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "shVIgEjrRmXBbXrhkzFzDgYputQrDpAx=AAtAGcAdAAwADsA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "toHOORYTzUXlSOjhXscBUqmMVmiMXsNo=YAD0AWwBpAG4AdA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "SKwLvZrVJVRvlVIDGDTNqJOPaHePepKc=AJABpACoAMAAuAD"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "KvfWnGVbFfbJqUyTlTmcnXmYTkPmOOOL=AUgBlAHMAaQB6AG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "qRAQESCSBsvELOYhnVXxhErEOMaGgAdq=AbABzAGUAewBbAH"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kCnywtgrOftGfOoytxYsGCOBqRjIXKVg=AKQBdADsAJAB0AH"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "SumVPsssZsmjsQaqRLjaHvfwOsgUlYpl=KAAkAHQAcwBYACo"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ocfetSwPhFdqkZZHsvgEpwWKPVbGETMo= JABDAGEAPQAiAC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LhSmgUOBztMJqkZdNnonqguvPsMQBdCy=BTAGUAdABDAHUAc"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jSRoBpHptCKVVleJGKfThDrhwbtnQClh=lAHMAaQB6AGUAKQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hkvEVLCsCxHbyADdoBMUzARTDXflDLPZ=ADEANwA5ACkAfQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YvAcvQuQWJGRCXPmmgjNTRdsEQhXLCwr=wA9ADAALgAwADIA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "WqkmcqIQqxQYRpyzeSgWyItjpOQQLGRS=MAbABlAGEAcgAtA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "qnUBaoyPVqcHgIOhSDARjcgyiIHgywfn=BlAHMAaQB6AGUAI"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "OsxzKOFvMOoYjYesFCzAqpTMwVIpBdKO=vAGwAZQBdADoAOg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kVapKTtTqiTkytGhxegsWoQRzRqGxJje=KgAoACQAdABjAFg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "dYiLVShXUvMyfcwLzYNrqokKwjNHOXJX=EAcgByAGEAeQAoA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YMxsRuRfyhWFvsPfKyVboBRVkLYqaCud=4AdABdADoAOgBPA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "mkJIdFuHCEnzTnTMpBdEQyaYFSdXXAxQ=DEAOAA1ADMAMAA3"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jViciqDLTDcZYLwsGLTnedkRbKaROxvt=ACkAXQA7ACQAYQB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "umkXoboQfxDjePlmOKMcrUQPOTCCLjVM=AWABZACoAJAB0AG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ufnBffrrGUFmwMHAHLDhRVFJEpzOzooJ=ACUANgAuADIAOAA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "gZmRpHxezhsRILiyGVGOneaqZbRdrpdt=A1ACkAXQA7ACQAd"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "newhJiLblUnVUwwAkzDTChonGDQJIcew=HMAUgBlAHMAaQB6"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ahvTBBIQTVJgGBOUFoBavjDvKDzFkvKB=QAYwBBAC0AJAB0A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "iefCZiVdWcHtnlIuAaRchfNBbuDcPxyr=AuAEMAbwB1AG4Ad"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "FMoLLpWQPszPtZdystOnBAnpusqrTBaW=MAQQApACoAJAB0A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "iqMxuJXtpeAZRYhpEEkcoATCFhUwRGWc=ABzAGMAWABZAD0A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kRMZCEqEysRfipsKOvbQpvSadgDXYNrc=AcwBCACkAKQA7AC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "arKPBEtdhtHUQYkWGHRiJPWbvebMgFxN=ACIAOwAkAHMAaQB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "tNPoZfMCQhfhUXJRTpTqOEmmYBWjJbwJ=BpAGwAZQAoACQAY"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "aitkKDuoRciujzIqkDDUZbisvFlwGncr=uAD0AQAAoAGYAbw"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YGVvRbiZHVUDLxAptNYGaupNVoUDPKBz=UAPQBAACgAZwBlA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "KQAkFsUCiaaPicSRWAQbAhMXuRuXNZoL=AOQAuADEANQApAF"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "wFdhBfgyqduRwhmudxvqDEBBikothwRd=EgAbwBzAHQAOwB3"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YjGujvNTMDQSJNOndadVEuACDmBagaHm=MQA1ADkALgAxADU"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "BnFiHxTuWRIFooWMiMgeNHBaXhGfbCms=AWwAoACQAYQBBAC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "FaAmgLNYIoRFVjvDPIogoNfuPwJpSLlZ=BTAGUAdABXAGkAb"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "lSKZwjYohjTLysyBDagvMgTOnvuINJvY=0AHMAQQAtACQAdA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "GRFtiLrPdCjqZQNlFuoqcTqkaoXNTDuE=B9ADsAJABhAFgAK"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "NmXYqjMvibVevFcctOdiRrUBSydediJf=JAB0AHMAWAAqACQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LqGmgRfhyNfnNkXnlvnzlbDAJRaUJyrK=BuAGcAXQA6ADoAa"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "EDsTKIwzFVCIMuWtcqyRaahWjwRslxqR=RAAqACgAJAB0AGM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "SeosBsyqyMqzdYFoLfEWjJalhZZFYGPT=qADEANQA5AC4AMQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "oxUTaVYhhQaspJryvNQkDgjjbgwIMxXy=powershell.exe "
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "wPRJEzhqXMSREdvNRmqyhhCDkYwLVmdA=ANAA0ACkAfQA7AE"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ZNKKhAdylixKFaXHQXsLkZVHHMgBJqXe=0AOwAkAHQAYwBCA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "fDPDRfUagzGTnrXogRwtPSjCBIuJzwEy=OQApAH0AKQA7ACQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "dCRkQpkZqrULJCWhguZbAdtLBDhAciLv=4ALAAtAH4AOgA7A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "EMrJTUgyWaUvFwZpaqQdNKKFzssFugbB=EAbgBkACQAaABhA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "pWWOaQSStbSseWlixbBkZvVgzHNXzlHg=0AOwAkAGEAQQArA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "OEeKmSiegAPQzlUEEmaybwMmArJCMZgR=AdABjAFkAPQAkAG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ZQPHPxBqWCAZvVQHlsGYiOlcuvIgsnbK=JABhAFkAJQA2AC4"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "TuoydMFiqykMRidIJzvumayFqnayjBEd=AWAAqACQARABwAC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "kmMRdIXSdVXfyOUpSOsmtflUeVdHQlrz=GEAWQAlADYALgAy"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "PEJqjaCeNdliDabGkgHRKHatStcyJRNV=ByACgAJABpAD0AM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "fEnwBkhUZDNBsrGHvySlauWFibfyQlPh=B0AF0AKAAyADAAK"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ENWxyqYsMgZHjejpyTOKmQzsRKLZIHus=oAJAB0AHMAQgArA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hTzKnfaoplvHXibPthZnAxoOXqGfmiig=AOwAkAGkAKwA9AD"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "FoRRhrobHMPDXPpEdcLpwpUBQcfFXWwP=ZAD0AMAA7AHcAaA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "VXRTfwIjkBLloykAQXXQcEjGkjGVGmtL=A6AG4AZQB3ACgAM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "sjeavIclFIJIxRjjWLUMtZoTUGjXAZHy=AEEAKQA7ACQAcwB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "qAlNKxQzYhbAsWUvCHAylYSdNtPmQicv=AqACgAKAAkAHQAc"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "gXCsOpcPNBtPWfxgXlIGlJbEAWjRwSuq=QBdADsAJAB0AHMA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "qmNAwJWOKFMElTDSZTDPasCJISxMDYcs=QAYQBBACUANgAuA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hOkQeXZBlLLvZgUhmbEzBNHFiBtsKEZr=HMAWAArADgAMAAq"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "KKtwBaHbtfAbwToNZzelSXakqzsqAuOB=ABzAGkAbgBbACgA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "TXZbqPbFgRNosuAqGMVcsYwliNfMHxnh=AG8AbgApAC4AUAB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "zSIbANTSHhgWYTWqiPucpefzArkIfSGh=BdACgANAAwACsAN"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "GjsQXERiwXrDvdnLHQjzLAvzVqfWcPKO=BtAC0AbABpAGsAZ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "DmvELHNMPEIhxoweyNxfLVeyotlMtuux=AC4AQwBvAG4AcwB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "olzaopsCixkixBkSdoyWDJXDTXvKnUmp=qADAALgAwADAANg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "cySokNQoXpxsFipTjOjLikwHIXxLPEQJ=QA7ACQAdABwAD0A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hVkrZnIhNezyNBfnlPyiMkLQqvuZrjGL=MAWAA9ACQAcwBpA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "epklJmUvXhNLrZozssCXGVIerLebCnKj=GkAPQAwADsAJABp"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "QISqOHsrafLHSPWewlAHhXvIZodqfTEI=AAnACAAJwAqADMA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "FbCuaMGtoJInCaNELUdXNbdyjbjDnPtw=wAyADAAKgAkAGkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "ZZLObrnpxHlXfeAkqPrQBzbJFFvdoZET=fQA7ACQAYQBZACs"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "tnIYqhNLiUorUDUKLEnDhdycdpljvLlR=AOwB3AGgAaQBsAG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "qdNcEpvvZGFUlnrAXkNhTQOvSvPTuHlk=AGUAKQB7AFsAdgB"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LWAzeuZwnbIcNdRjxhOIqeaDiYgAvDrx=QQAtACQAdABzAGM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "CaIirQAqTefpbmTXWMyrgmsWquInUCZy=AJABEAHAAKgAkAH"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "nOkJJPdmctXAXylvCfaghZLvMnTmCDWc=kARAA9ADEALwAoA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "gEaZOTjvvrngeLzimmGQLDwkUpqCkUvH=0AJABpAEQAOwAkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "uWHIJcocpzjzGQYRJKaXbdGNXvoTAMGw=AYwBvAHMAPQBAAC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "AGYoVyIwYqxPlEYRDtApgacGtptLIHkm=AbwBDAGgAYQByAE"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "pUaHSFQwRSvRvsDPqCryasbWiPZjVTlz=AcgBvAG4AbQBlAG"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "vuAIcMCRuXBYqrrUNZmOcYfcjixddjtZ=AcwBpAG4AWwAoAC"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LOrIeypmQCDrtyrBxVvcSfcGDEyNeLWl=AyADgAMwAxADgAN"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "vMOyRrLZQhMayzUymNIOeNtZaBHxJVYv=gBzAG8AcgBQAG8A"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "HWdWbiYeRRZmgvvpeQtTNohfhonorRBl=G8AbABlAF0AOgA6"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "BuQXExtIoJenDCoDWMllAGBrQRTtpPDx=ADgAKgAxADUAOQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "qLNXYBdkzwEMgZtwqCPMBXgVSSfuhTjF=pADsAJABpAHMAVQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "plxEJcjrSebITEMMRDSrBhYuJablezVe=sAGEAdABmAG8Acg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "JoXrdwtvualmMzOVzaOsXMhkzDgFNpAw=aQBmACgAJABpAHM"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "xuIZfcXrxtSqOZNUDduUHcibteSjyxng=sAGUAWwBdAF0AOg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "IbbabjgpfkTotnduCnPMSTGIsOckMiWr=OgA6AEMAbwBzACg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "YOkRLgnIGXkOpXWvtjXJfCSxQIHicopo=vAGkAZABdACgAcg"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "rcftLiugePWLsjKVZASGgzZksyHRjcqn=LgAyADgAKQB7ACQ"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "wNanBtTuUhqfZLnNoHtSNLgGSsVujLHd=uADEANQApAF0AOw"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "fNGaSKRntOuLzmEbIBoiGiWALDRbynQZ=D0AMAAuADAAOQA7"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "LWOapEqzpUskxaQsOaVkhcJSEQmLZShR=QAaQBkAHgAPQAkA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "xVtjEmnPGIQuHEpArmceHVBoYNiHPzOl=AAwACoAJABpAEQA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "hbmTfcfcjkrbonYbtLItMcEAmrgrVcti=QA2AC4AMgA4ACoA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "jwpUaFXNEasCpVbptAKSnEDarpTLMPat=UAKAAkAGEAWAAtA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "GLYMalYAdURNgeYgcnRRyqjEQeDIgheb=LgAyADgAKgAxADU"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "boJZOUChltoSFKfXbQaVsOxdbqcBWcvP=GwAdAA2AC4AMgA4"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "XdpMnouQKzDFtodMsSbDkkuLSzaLLiHB=AAkAGEAQQAlADYA"
!goMzBiWYAvJaKWYzsCQybYPAgeLbSihV! "oNlpyTGkGeJPKddRSswWvoLiawmsCBVm=G8AQQBbACQAaQBk"
%oxUTaVYhhQaspJryvNQkDgjjbgwIMxXy%%CEQMPgYqlQxWxtiRdHExpELpNyceoqlv%%ocfetSwPhFdqkZZHsvgEpwWKPVbGETMo%%dCRkQpkZqrULJCWhguZbAdtLBDhAciLv%%WTTZBzBmsmAaZFqacGySDiNYNGylcCTy%%arKPBEtdhtHUQYkWGHRiJPWbvebMgFxN%%aitkKDuoRciujzIqkDDUZbisvFlwGncr%%PEJqjaCeNdliDabGkgHRKHatStcyJRNV%%STWQdRclSfbmBAQTetBNxIMqkcEhGDTN%%ptaipqfUzgRBDAbaaRzHpjvAtCZtYrNy%%hTzKnfaoplvHXibPthZnAxoOXqGfmiig%%oHPhevdnirNKRiTIWCDXxGAqqRfMbvJn%%ToqxmNWSbEKXYwTvINOVReKKlrXTPGqK%%QVYlBQUOpMRSdlQRadVYGDNyzGdKgVCd%%olzaopsCixkixBkSdoyWDJXDTXvKnUmp%%LOrIeypmQCDrtyrBxVvcSfcGDEyNeLWl%%brGSmTGfxzlgdHPsbLnwyflefhAmOgCQ%%fDPDRfUagzGTnrXogRwtPSjCBIuJzwEy%%uWHIJcocpzjzGQYRJKaXbdGNXvoTAMGw%%LEFcUeBTsDGSrPjCFtfNrCLXaCdmtFvK%%epklJmUvXhNLrZozssCXGVIerLebCnKj%%wmujLTvoHNsZXfzIKHgjlgBTKkseGYAm%%EkvWOoMrCYjdyOUTsVeaUMpCDrLJhYll%%BGJbJEmvqWXlhEmnMaXOUtXWXwxOQzen%%ljAagDUzzHoRQgRPqcvFLlgcRTHOKJXB%%IbbabjgpfkTotnduCnPMSTGIsOckMiWr%%SKwLvZrVJVRvlVIDGDTNqJOPaHePepKc%%SqeWuHZDDCjQkfKHEyOPqQYaxxAqFfKg%%mkJIdFuHCEnzTnTMpBdEQyaYFSdXXAxQ%%hkvEVLCsCxHbyADdoBMUzARTDXflDLPZ%%qLNXYBdkzwEMgZtwqCPMBXgVSSfuhTjF%%mqcuvQXOncXQjGoCcOSnLyYZOFbnetnI%%pPURVMhdoeeBVAVPsSwBlGoBvzGKLlCZ%%yzERozVHUASWEpSiSvfaoPsWBNnrZZfo%%pUaHSFQwRSvRvsDPqCryasbWiPZjVTlz%%YMxsRuRfyhWFvsPfKyVboBRVkLYqaCud%%jlIfqnzaijSQSqZgBkuwdPGaRpVaBSOb%%TXZbqPbFgRNosuAqGMVcsYwliNfMHxnh%%plxEJcjrSebITEMMRDSrBhYuJablezVe%%GjsQXERiwXrDvdnLHQjzLAvzVqfWcPKO%%rkwJRmooqgDqJFkMOOgrZksAvLrCUowb%%mjubFPCGjKvuVBezPzSLKgPiMkiLHCdC%%KvfWnGVbFfbJqUyTlTmcnXmYTkPmOOOL%%YGVvRbiZHVUDLxAptNYGaupNVoUDPKBz%%XepkkVqYvTtgdFENPhzcJWYCpcLoaqit%%wIaGQfGdGRDhDlraSbCuXcmZLLHpuGLW%%jSRoBpHptCKVVleJGKfThDrhwbtnQClh%%iefCZiVdWcHtnlIuAaRchfNBbuDcPxyr%%shVIgEjrRmXBbXrhkzFzDgYputQrDpAx%%JoXrdwtvualmMzOVzaOsXMhkzDgFNpAw%%SfvwzzERAepjpyGMFHUNKrROqssnPuNm%%EMrJTUgyWaUvFwZpaqQdNKKFzssFugbB%%newhJiLblUnVUwwAkzDTChonGDQJIcew%%qdNcEpvvZGFUlnrAXkNhTQOvSvPTuHlk%%YOkRLgnIGXkOpXWvtjXJfCSxQIHicopo%%qnUBaoyPVqcHgIOhSDARjcgyiIHgywfn%%liGWHfIyrVLwBEIwCOiYyPRiqGDdbyox%%KAmgANemAlJpcDDjSjiBHHQOISGMnSdc%%qRAQESCSBsvELOYhnVXxhErEOMaGgAdq%%rINfcbMjKAxjURqPPWkqpoSTEHAxKarK%%cycScIVrKpjzpRGeEUNoVdsdoCmithqQ%%DmvELHNMPEIhxoweyNxfLVeyotlMtuux%%OsxzKOFvMOoYjYesFCzAqpTMwVIpBdKO%%FaAmgLNYIoRFVjvDPIogoNfuPwJpSLlZ%%eeqXaNZTFaroLDIZzdsBwkmHOIJjhshD%%QhPcvIJHDFyHBFcMQviAXIpkGmVncGKg%%wPRJEzhqXMSREdvNRmqyhhCDkYwLVmdA%%WqkmcqIQqxQYRpyzeSgWyItjpOQQLGRS%%wFdhBfgyqduRwhmudxvqDEBBikothwRd%%fSpnCzemWQljcMezqUQPjzwVbTLqelSW%%zoPVtOMmmEnhuXtBapsLGUmEggDDgtUi%%kLMmjMcAFmaEOhAoaFlmcMglZmWogxjW%%QISqOHsrafLHSPWewlAHhXvIZodqfTEI%%jqSJKOiGCInmfGKbWlvBIUuOfDDAymTY%%AGYoVyIwYqxPlEYRDtApgacGtptLIHkm%%dYiLVShXUvMyfcwLzYNrqokKwjNHOXJX%%fZjxnFMQbToFTXDlyrHihFeADhsbcrjq%%YtRObiLwsePyLxOMHKKNGQoTqOWOuPss%%xuIZfcXrxtSqOZNUDduUHcibteSjyxng%%VXRTfwIjkBLloykAQXXQcEjGkjGVGmtL%%hfxbBziXZTOUaMkmmFtaXEdFjAnHgQaO%%tYVHRnVTOXjGjozaoCuLXwfPssunnXsz%%vuAIcMCRuXBYqrrUNZmOcYfcjixddjtZ%%qmNAwJWOKFMElTDSZTDPasCJISxMDYcs%%EtVeFpgjxzLWMkQIkYTMXfyrAyEhDNMo%%kzkNIUTsmcyUECtdkEmWIudjTaDSmmIa%%slhijcLafreHgjmZMyKvBfQFkEdihJWF%%BdVOuSXgXiCeCtefzDtMEppxIyxPWIrK%%XdpMnouQKzDFtodMsSbDkkuLSzaLLiHB%%GLYMalYAdURNgeYgcnRRyqjEQeDIgheb%%KQAkFsUCiaaPicSRWAQbAhMXuRuXNZoL%%ZNKKhAdylixKFaXHQXsLkZVHHMgBJqXe%%REMLtrqsINbvWvnIuECkKbOzTGBenqZG%%hwFhwJaxXXdwurvhjKTtBiyEGJzzsknX%%OErjrJJJBZgZWibHDnODruTqexbqRNYD%%kEsDHxRPdKtbCQywAFGgTGehyDuboOJF%%gXCsOpcPNBtPWfxgXlIGlJbEAWjRwSuq%%kvQdbfQQbCnjvidcKGqeQOPlbnPHtEvR%%BnFiHxTuWRIFooWMiMgeNHBaXhGfbCms%%zsrSJGmSJnyHokBtHeFgsIKrxXUExBai%%TpdJIGdxYfXInfrEXiTgSWEDRkILnwAw%%jViciqDLTDcZYLwsGLTnedkRbKaROxvt%%FoRRhrobHMPDXPpEdcLpwpUBQcfFXWwP%%tNPoZfMCQhfhUXJRTpTqOEmmYBWjJbwJ%%NgZCJWBeVjPKRQGtswEGJatjgnpzjgWk%%rcftLiugePWLsjKVZASGgzZksyHRjcqn%%OEeKmSiegAPQzlUEEmaybwMmArJCMZgR%%hnFLnLggClXqYcdrNJDeJKmckpJwwnOj%%kmMRdIXSdVXfyOUpSOsmtflUeVdHQlrz%%BuQXExtIoJenDCoDWMllAGBrQRTtpPDx%%wNanBtTuUhqfZLnNoHtSNLgGSsVujLHd%%UZJJmpuaOhJarhzMsJJbslRfNgGWbcrj%%KKtwBaHbtfAbwToNZzelSXakqzsqAuOB%%ZQPHPxBqWCAZvVQHlsGYiOlcuvIgsnbK%%ZekWFDOMmhMPlBqRMUjvUDXUuVmJfLYB%%lwKHmWMAemXrTFXsgSVDbHhhvuoMPbFg%%ixiedIlDwYMVOrKwrVXvPoQCEYFMovhS%%sylTwayROvSFYsBcxNRbPwSkBRbtfuOY%%LbSFrrIlqizStWtSCEWjhMdmQSBeyDLU%%KDvsZeOebWuOoESvFtyGqmAFdkycfhSr%%XWmBIDMOINqEFufJgfAFAhTWhkDjuFhp%%gJmLmphKnpetZFMauKXywqlBTCsaTADc%%tnIYqhNLiUorUDUKLEnDhdycdpljvLlR%%jwpUaFXNEasCpVbptAKSnEDarpTLMPat%%boJZOUChltoSFKfXbQaVsOxdbqcBWcvP%%SXRgnlxHwZQFcUbJjQQTXxcoGhZWZDBH%%GdOBcywxUNEHhnDvcZAAShNCwtrIdSsZ%%QwFMjLnlQEwKCPCMAeQKLjAYLcLDGTLq%%hbmTfcfcjkrbonYbtLItMcEAmrgrVcti%%YjGujvNTMDQSJNOndadVEuACDmBagaHm%%kCnywtgrOftGfOoytxYsGCOBqRjIXKVg%%hVkrZnIhNezyNBfnlPyiMkLQqvuZrjGL%%KOtoZJlKPfZyJNNWdeKhxZLujrwGuYlr%%ufnBffrrGUFmwMHAHLDhRVFJEpzOzooJ%%SeosBsyqyMqzdYFoLfEWjJalhZZFYGPT%%gZmRpHxezhsRILiyGVGOneaqZbRdrpdt%%iqMxuJXtpeAZRYhpEEkcoATCFhUwRGWc%%NmXYqjMvibVevFcctOdiRrUBSydediJf%%lfQVtlqXUBKQhqxykWXUowHxNQLFAwWj%%nOkJJPdmctXAXylvCfaghZLvMnTmCDWc%%DTZRcqBGYKXfDEZLmzDJYpxSeSZfcpuA%%XKNepqGxWuXWAneqLZBfpNpeMaPMiEPW%%DlfMpbbeCJJcQPwvkvdHmAQpSkaRYThd%%pNOhLHBPnAsxIAGRyWyPVsYRDknXkkKc%%cySokNQoXpxsFipTjOjLikwHIXxLPEQJ%%SumVPsssZsmjsQaqRLjaHvfwOsgUlYpl%%CaIirQAqTefpbmTXWMyrgmsWquInUCZy%%ahvTBBIQTVJgGBOUFoBavjDvKDzFkvKB%%ycsjwqPScCTZmZYRuwUbdabuFUUobHkb%%sjeavIclFIJIxRjjWLUMtZoTUGjXAZHy%%toHOORYTzUXlSOjhXscBUqmMVmiMXsNo%%zSIbANTSHhgWYTWqiPucpefzArkIfSGh%%xVtjEmnPGIQuHEpArmceHVBoYNiHPzOl%%kVapKTtTqiTkytGhxegsWoQRzRqGxJje%%jfIuNshxMRUEtJIVVKInMlCXZOiywmQc%%BAQLsAMjcAsfCyDIVmMTcopZVILYFYSX%%jswCBpKVgXcoKEAgWMguzXkKkzShQdgJ%%yTqIOVRqNAAMQDvDGTXLQpKevUwoVOLp%%IMSTJemmkhVkPoZYPKgqYJzjfMujNwnW%%fEnwBkhUZDNBsrGHvySlauWFibfyQlPh%%FbCuaMGtoJInCaNELUdXNbdyjbjDnPtw%%EDsTKIwzFVCIMuWtcqyRaahWjwRslxqR%%TuoydMFiqykMRidIJzvumayFqnayjBEd%%ENWxyqYsMgZHjejpyTOKmQzsRKLZIHus%%OisiVKqrEwDsENvzFHUOcjxBVukowIZV%%DisqpJBGBnHuxeKjsLqZAfBexpjYjULQ%%fKFYUGzJFsyCsmrHbbkviDKjwdZczXVw%%qAlNKxQzYhbAsWUvCHAylYSdNtPmQicv%%YKCNVtmHWjqXwgLEMSSgfctMWANymuls%%LWAzeuZwnbIcNdRjxhOIqeaDiYgAvDrx%%umkXoboQfxDjePlmOKMcrUQPOTCCLjVM%%FMoLLpWQPszPtZdystOnBAnpusqrTBaW%%JOglywWAIIsXCqGEZzUHtBOjkILITPTA%%CJmbLKYSpSHaVvAIuyTKuvqNElKICJST%%lSKZwjYohjTLysyBDagvMgTOnvuINJvY%%YPrykEGvigaqHWulohvKVTCDSKYQlykv%%vxPYQLoxBpHEsVdnWeiTxfVYzYCzUdJO%%stWFhDhIxyTBqcKJmslzJobJghbSgidc%%kRMZCEqEysRfipsKOvbQpvSadgDXYNrc%%LWOapEqzpUskxaQsOaVkhcJSEQmLZShR%%hOkQeXZBlLLvZgUhmbEzBNHFiBtsKEZr%%mJsTvjOmhCuHUZStoYtwxaSKAcpJamRT%%MKUuLXYcUksyDzwSFAINQuWOpDmfQQBU%%BOTqHlmSybXEmMephXiFVlJKRUTzXHmg%%vJYyKAkppkrSUFKOPojnhInjWvyUNloG%%hkPfdmeOzmSoKUlfKZRMdBPsmnTFtFIG%%sTgSpkZNpfMwsQZKwxRhxbqBPSqzDerL%%gEaZOTjvvrngeLzimmGQLDwkUpqCkUvH%%oNlpyTGkGeJPKddRSswWvoLiawmsCBVm%%HPzXLBGfRiefAGnRgxpQfXuOXAeScgZH%%WxtnaIOxXarzDBUHVtoGwgzRLaKnKPAT%%GRFtiLrPdCjqZQNlFuoqcTqkaoXNTDuE%%YvAcvQuQWJGRCXPmmgjNTRdsEQhXLCwr%%ZZLObrnpxHlXfeAkqPrQBzbJFFvdoZET%%ZgOwNCysxFAImHbFxbdOzmOPkHnzigAV%%pWWOaQSStbSseWlixbBkZvVgzHNXzlHg%%fNGaSKRntOuLzmEbIBoiGiWALDRbynQZ%%RFiXVFEzPnjiElmrmfkRbKcBhZcmDbmb%%OOchLjtCSWQTGfEqeckusbWVNElxNNBG%%LhSmgUOBztMJqkZdNnonqguvPsMQBdCy%%vMOyRrLZQhMayzUymNIOeNtZaBHxJVYv%%YHCTMKZWGLUyWcuqKoVzlzUVHgcxnEpH%%YgMdTeeJklQMgWrqSJcZhOrqzinJZgcs%%YUqXMkwPwQFUcNTkoeQaanjOfbbOutBp%%HWdWbiYeRRZmgvvpeQtTNohfhonorRBl%%juArooPrSdQtBTrZjJvpfxPDHXfJSYIm%%FZfjncfWBkxIjcTOXMXoGCeQUxAhpqMX%%LqGmgRfhyNfnNkXnlvnzlbDAJRaUJyrK%%HaEBevbEDivBppnoSCvoCiXkggxNqnXK%%HYQPWJzyNfiBzLrZRFxziQlXFyizLYDh%%uVuQqHKduINTSHcvZDZGwIHMbrTyuViN%
```
