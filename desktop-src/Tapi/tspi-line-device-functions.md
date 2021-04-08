---
description: Esta seção contém uma lista alfabética das funções de dispositivo de linha disponíveis no SPI de telefonia.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Funções de dispositivo de linha TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828673"
---
# <a name="tspi-line-device-functions"></a>Funções de dispositivo de linha TSPI

Esta seção contém uma lista alfabética das funções de dispositivo de linha disponíveis no SPI de telefonia. As informações para cada função incluem o seguinte:

-   Uma instrução da finalidade da função.
-   A sintaxe correta para a função.
-   Uma descrição dos parâmetros da função, incluindo Estados de chamada válidos.
-   Uma descrição do valor de retorno da função.
-   Uma seção de comentários que pode incluir qualquer ou todas as seguintes opções: uma lista dos Estados de chamada válidos na entrada da função e as transições de estado de chamada típicas quando a solicitação for concluída; uma descrição de quais membros de grandes estruturas de dados devem ser preenchidos pelo provedor de serviços e quais membros devem ter seus valores preservados intactos; e comparação com uma função correspondente dentro da TAPI.
-   Referências a outras funções, mensagens ou estruturas de dados.
    > [!Note]  
    > Os Estados reais nos quais uma função pode ser executada podem ser limitados pelos recursos do provedor de serviços. Os provedores de serviço devem definir o membro **dwCallFeatures** na estrutura [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) , o membro **dwAddressFeatures** na estrutura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) e o membro **dwLineFeatures** na estrutura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) para indicar aos aplicativos se uma função é permitida ou não nesse ponto no tempo.

     

Esta seção contém as seguintes funções de dispositivo TSPI line:

-   [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**TSPI \_ lineAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**TSPI \_ lineBlindTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [TSPI \_ lineDropNoOwner](tspi-linedropnoowner.md)
-   [TSPI \_ lineDropOnClose](tspi-linedroponclose.md)
-   [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ lineGatherDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**TSPI \_ lineGenerateTone**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**TSPI \_ lineGetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**TSPI \_ lineGetCallIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**TSPI \_ lineGetExtensionID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**TSPI \_ lineGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**TSPI \_ lineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**TSPI \_ lineMonitorMedia**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**TSPI \_ lineMonitorTones**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**TSPI \_ linePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**TSPI \_ lineRedirect**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**TSPI \_ lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**TSPI \_ lineRemoveFromConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**TSPI \_ lineSecureCall**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**TSPI \_ lineSendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**TSPI \_ lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI \_ lineSetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**TSPI \_ lineSetCallParams**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**TSPI \_ lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI \_ lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [TSPI \_ lineSetCurrentLocation](tspi-linesetcurrentlocation.md)
-   [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**TSPI \_ lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI \_ lineSetMediaControl**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**TSPI \_ lineSetMediaMode**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineSwapHold**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**TSPI \_ lineUncompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**TSPI \_ lineUnhold**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
