---
description: As funções a seguir são fornecidas apenas em uma versão genérica sem um &\# 0034; Um&\# 0034; ou &\# 0034; W&\# 0034; sufixo.
ms.assetid: 0e51b7a6-53a0-4e92-9bed-f8e4f8ffd5a1
title: Funções sem versões Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a5b2444aa32a6ad5b7825c17b31ea66eaacf91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472892"
---
# <a name="functions-without-unicode-versions"></a>Funções sem versões Unicode

As funções a seguir são fornecidas apenas em uma versão genérica sem um sufixo "A" ou "W".




| Função TAPI | Comentários | 
|---------------|----------|
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaccept"><strong>lineAccept</strong></a> | Presume-se que a memória apontada por <em>lpsUserUserInfo</em> contenha dados binários para transferência de ponta a ponta. O aplicativo deve fornecer dados em um formulário pronto para transmissão. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference"><strong>Lineaddtoconference</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineagentspecific"><strong>lineAgentSpecific</strong></a> | A memória apontada por <em>lpParams</em> é privada entre o aplicativo e o manipulador de agente. O aplicativo deve fornecer dados no formulário especificado na definição de extensão do manipulador do agente. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineanswer"><strong>Lineanswer</strong></a> | Presume-se que a memória apontada por <em>lpsUserUserInfo</em> contenha dados binários para transferência de ponta a ponta. O aplicativo deve fornecer dados em um formulário pronto para transmissão. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineclose"><strong>Lineclose</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linecompletecall"><strong>lineCompleteCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer"><strong>Linecompletetransfer</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider"><strong>lineConfigProvider</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall"><strong>Linedeallocatecall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedevspecific"><strong>lineDevSpecific</strong></a> | A memória apontada por <em>lpParams</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve fornecer dados no formulário especificado na definição de extensão do provedor de serviços. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature"><strong>lineDevSpecificFeature</strong></a> | A memória apontada por <em>lpParams</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve fornecer dados no formulário especificado na definição de extensão do provedor de serviços. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedrop"><strong>Linedrop</strong></a> | Presume-se que a memória apontada por <em>lpsUserUserInfo</em> contenha dados binários para transferência de ponta a ponta. O aplicativo deve fornecer dados em um formulário pronto para transmissão. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegeneratetone"><strong>Linegeneratetone</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus"><strong>Linegetcallstatus</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls"><strong>lineGetConfRelatedCalls</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls"><strong>lineGetNewCalls</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetmessage"><strong>Linegetmessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetnumrings"><strong>lineGetNumRings</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages"><strong>lineGetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linehold"><strong>lineHold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitordigits"><strong>lineMonitorDigits</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitormedia"><strong>Linemonitormedia</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitortones"><strong>lineMonitorTones</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion"><strong>Linenegotiateapiversion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion"><strong>lineNegotiateExtVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineproxymessage"><strong>lineProxyMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse"><strong>lineProxyResponse</strong></a> | Os campos na estrutura <a href="/windows/win32/api/tapi/ns-tapi-lineproxyrequest"><strong>LINEPROXYREQUEST</strong></a> são sempre Unicode. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient"><strong>lineRegisterRequestRecipient</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo"><strong>lineReleaseUserUserInfo</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference"><strong>lineRemoveFromConference</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider"><strong>lineRemoveProvider</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesecurecall"><strong>lineSecureCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo"><strong>lineSendUserUserInfo</strong></a> | Presume-se que a memória apontada por <em>lpsUserUserInfo</em> contenha dados binários para transferência de ponta a ponta. O aplicativo deve fornecer dados em um formulário pronto para transmissão. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity"><strong>lineSetAgentActivity</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup"><strong>lineSetAgentGroup</strong></a> | <blockquote>[!Note]<br />Os nomes de grupo são ignorados.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentstate"><strong>lineSetAgentState</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetappspecific"><strong>lineSetAppSpecific</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcalldata"><strong>lineSetCallData</strong></a> | A memória apontada por <em>lpCallData</em> está em um formato especificado pelo aplicativo ou um grupo de aplicativos de formatação. O formato dos dados está além do escopo da TAPI e não é convertido pela TAPI. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallparams"><strong>lineSetCallParams</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege"><strong>lineSetCallPrivilege</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice"><strong>lineSetCallQualityOfService</strong></a> | O formato de dados na parte específica do provedor da estrutura QOS está além do escopo da TAPI e não é convertido pela TAPI. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment"><strong>lineSetCallTreatment</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation"><strong>lineSetCurrentLocation</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus"><strong>lineSetLineDevStatus</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol"><strong>lineSetMediaControl</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetmediamode"><strong>lineSetMediaMode</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetnumrings"><strong>Linesetnumrings</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages"><strong>lineSetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetterminal"><strong>Linesetterminal</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineshutdown"><strong>Lineshutdown</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineswaphold"><strong>Lineswaphold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall"><strong>lineUncompleteCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineunhold"><strong>lineUnhold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneclose"><strong>phoneClose</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonedevspecific"><strong>phoneDevSpecific</strong></a> | A memória apontada por <em>lpParams</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve fornecer dados no formulário especificado na definição de extensão do provedor de serviços. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdata"><strong>phoneGetData</strong></a> | A memória apontada por <em>lpData</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve processar dados no formulário especificado na definição do provedor de serviços. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay"><strong>phoneGetDisplay</strong></a> | A memória apontada por <em>lpDisplay</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve processar dados no formulário especificado na definição do provedor de serviços. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetgain"><strong>phoneGetGain</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch"><strong>phoneGetHookSwitch</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetlamp"><strong>phoneGetLamp</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetmessage"><strong>phoneGetMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetring"><strong>phoneGetRing</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages"><strong>phoneGetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetvolume"><strong>phoneGetVolume</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion"><strong>Phonenegotiateapiversion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion"><strong>phoneNegotiateExtVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneopen"><strong>phoneOpen</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetdata"><strong>phoneSetData</strong></a> | A memória apontada por <em>lpParams</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve fornecer dados no formato especificado na definição do provedor de serviço. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay"><strong>phoneSetDisplay</strong></a> | A memória apontada por <em>lpDisplay</em> é privada entre o aplicativo e o provedor de serviços. O aplicativo deve fornecer dados no formato especificado na definição do provedor de serviço. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetgain"><strong>phoneSetGain</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch"><strong>phoneSetHookSwitch</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetlamp"><strong>phoneSetLamp</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetring"><strong>phoneSetRing</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages"><strong>phoneSetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetvolume"><strong>phoneSetVolume</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneshutdown"><strong>phoneShutdown</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-tapirequestdrop"><strong>tapiRequestDrop</strong></a> | Essa função está obsoleta e não está disponível para aplicativos. | 
| <a href="tapirequestmediacall.md"><strong>tapiRequestMediaCall</strong></a> | Essa função está obsoleta e não está disponível para aplicativos. | 




 

 

 




