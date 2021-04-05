---
description: Gerencia relatórios de endereços cívicos.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Objeto LocationDisp. CivicAddressReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662748"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>Objeto LocationDisp. CivicAddressReportFactory

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Gerencia relatórios de endereços cívicos.

## <a name="members"></a>Membros

O objeto **LocationDisp. CivicAddressReportFactory** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **LocationDisp. CivicAddressReportFactory** tem esses métodos.



| Método                                                                                            | Descrição                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Solicita eventos de relatório de endereços cívicos.<br/>                                              |
| [**RequestPermissions**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.<br/> |
| [**StopListeningForReports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Cancela as solicitações de evento de relatório de endereço cívico.<br/>                                       |



 

### <a name="properties"></a>Propriedades

O objeto **LocationDisp. CivicAddressReportFactory** tem essas propriedades.



| Propriedade                                                                                        | Tipo de acesso           | Descrição                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Somente leitura<br/>  | O [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)atual.<br/> |
| [**DesiredAccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Leitura/gravação<br/> | A configuração de precisão desejada atual.<br/>                                                           |
| [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Leitura/gravação<br/> | O intervalo de eventos de relatório de endereços do cívico atual em milissegundos.<br/>                                |
| [**Status**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Somente leitura<br/>  | O status atual do relatório.<br/>                                                                      |



 

## <a name="examples"></a>Exemplos

O código de exemplo a seguir mostra como criar esse objeto em código HTML.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



O código de exemplo a seguir mostra como criar esse objeto em JScript usando o Windows Script Host.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



O código de exemplo a seguir mostra como criar esse objeto em VBScript usando o Windows Script Host.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LocationDisp.CivicAddressReport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

