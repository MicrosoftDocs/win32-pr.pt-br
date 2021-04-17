---
description: Representa um relatório de endereços cívicos.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Objeto LocationDisp. DispCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757243"
---
# <a name="locationdispdispcivicaddressreport-object"></a>Objeto LocationDisp. DispCivicAddressReport

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Representa um relatório de endereços cívicos.

## <a name="members"></a>Membros

O objeto **LocationDisp. DispCivicAddressReport** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **LocationDisp. DispCivicAddressReport** tem essas propriedades.



| Propriedade                                                                              | Tipo de acesso          | Descrição                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Somente leitura<br/> | A primeira linha de um endereço.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Somente leitura<br/> | A segunda linha de um endereço de rua.<br/>             |
| [**City**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Somente leitura<br/> | O nome da cidade.<br/>                                   |
| [**CountryRegion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Somente leitura<br/> | O nome do país ou da região.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Somente leitura<br/> | O nível de detalhe do relatório.<br/>                 |
| [**PostalCode**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Somente leitura<br/> | O código postal.<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Somente leitura<br/> | O nome do Estado ou da província.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Somente leitura<br/> | A data e a hora em que o relatório foi gerado.<br/> |



 

## <a name="remarks"></a>Comentários

Você pode recuperar esse objeto por meio da propriedade [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) de um objeto [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) . Você pode receber esse objeto por meio do evento [**NewCivicAddressReport**](newcivicaddressreport.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

