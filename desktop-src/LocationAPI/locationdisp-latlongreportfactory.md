---
description: Gerencia relatórios de latitude/longitude.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Objeto LocationDisp. LatLongReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837326"
---
# <a name="locationdisplatlongreportfactory-object"></a>Objeto LocationDisp. LatLongReportFactory

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Gerencia relatórios de latitude/longitude.

## <a name="members"></a>Membros

O objeto **LocationDisp. LatLongReportFactory** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **LocationDisp. LatLongReportFactory** tem esses métodos.



| Método                                                                                       | Descrição                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-latlongreportfactory-listenforreports.md)               | Solicita eventos de relatório de latitude/longitude.<br/>                                         |
| [**RequestPermissions**](locationdisp-latlongreportfactory-requestpermissions.md)           | Abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.<br/> |
| [**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Cancela solicitações de eventos de relatório de latitude/longitude.<br/>                             |



 

### <a name="properties"></a>Propriedades

O objeto **LocationDisp. LatLongReportFactory** tem essas propriedades.



| Propriedade                                                                                | Tipo de acesso           | Descrição                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**DesiredAccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Leitura/gravação<br/> | O valor de precisão desejado atual.<br/>                                                   |
| [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Somente leitura<br/>  | O [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)atual.<br/> |
| [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Leitura/gravação<br/> | O intervalo de eventos de relatório de latitude/longitude atual em milissegundos.<br/>                 |
| [**Status**](locationdisp-latlongreportfactory-status.md)<br/>                   | Somente leitura<br/>  | O status atual do relatório.<br/>                                                            |



 

## <a name="examples"></a>Exemplos

O código de exemplo a seguir mostra como criar esse objeto em código HTML.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



O código de exemplo a seguir mostra como criar esse objeto em JScript usando o Windows Script Host.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



O código de exemplo a seguir mostra como criar esse objeto em VBScript usando o Windows Script Host.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

