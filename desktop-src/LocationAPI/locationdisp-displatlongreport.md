---
description: Representa um relatório de latitude/longitude.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Objeto LocationDisp. DispLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784105"
---
# <a name="locationdispdisplatlongreport-object"></a>Objeto LocationDisp. DispLatLongReport

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Representa um relatório de latitude/longitude.

## <a name="members"></a>Membros

O objeto **LocationDisp. DispLatLongReport** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **LocationDisp. DispLatLongReport** tem essas propriedades.



| Propriedade                                                                         | Tipo de acesso          | Descrição                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Altitude**](locationdisp-displatlongreport-altitude.md)<br/>           | Somente leitura<br/> | Altitude atual, em metros.<br/>                                                                                                                                                           |
| [**AltitudeError**](locationdisp-displatlongreport-altitudeerror.md)<br/> | Somente leitura<br/> | Erro de altitude, em metros.<br/>                                                                                                                                                             |
| [**ErrorRadius**](locationdisp-displatlongreport-errorradius.md)<br/>     | Somente leitura<br/> | Uma distância do local relatado, em metros. Combinado com o local relatado como a origem, esse raio descreve o círculo no qual o local real é proably localizado.<br/> |
| [**Latitude**](locationdisp-displatlongreport-latitude.md)<br/>           | Somente leitura<br/> | Latitude atual, em graus.<br/>                                                                                                                                                          |
| [**Longitude**](locationdisp-displatlongreport-longitude.md)<br/>         | Somente leitura<br/> | Longitude atual, em graus.<br/>                                                                                                                                                         |
| [**Timestamp**](locationdisp-displatlongreport-timestamp.md)<br/>         | Somente leitura<br/> | A data e a hora em que o relatório foi gerado.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Você pode recuperar esse objeto por meio da propriedade [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) do objeto [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) . Você pode receber esse objeto por meio do evento [**NewLatLongReport**](newlatlongreport.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

