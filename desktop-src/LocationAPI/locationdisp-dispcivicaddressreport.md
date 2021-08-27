---
description: Representa um relatório de endereço civil.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Objeto LocationDisp.DispCivicAddressReport
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
ms.openlocfilehash: e5646bd6df1a2523faf481bc867acc67dbd0a647b4cdf3f033d7327a66174d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129976"
---
# <a name="locationdispdispcivicaddressreport-object"></a>Objeto LocationDisp.DispCivicAddressReport

\[O modelo de objeto da API de Localização está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de Geolocalização do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo da área de trabalho, use o [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Representa um relatório de endereço civil.

## <a name="members"></a>Membros

O **objeto LocationDisp.DispCivicAddressReport** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto LocationDisp.DispCivicAddressReport** tem essas propriedades.



| Propriedade                                                                              | Tipo de acesso          | Descrição                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Somente leitura<br/> | A primeira linha de um endereço de rua.<br/>              |
| [**Addressline2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Somente leitura<br/> | A segunda linha de um endereço de rua.<br/>             |
| [**City**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Somente leitura<br/> | O nome da cidade.<br/>                                   |
| [**Countryregion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Somente leitura<br/> | O nome do país ou da região.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Somente leitura<br/> | O nível de detalhes do relatório.<br/>                 |
| [**Postalcode**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Somente leitura<br/> | O código postal.<br/>                                 |
| [**Stateprovince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Somente leitura<br/> | O nome do estado ou da província.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Somente leitura<br/> | A data e a hora em que o relatório foi gerado.<br/> |



 

## <a name="remarks"></a>Comentários

Você pode recuperar esse objeto por meio da [**propriedade CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) de um [**objeto CivicAddressReportFactory.**](locationdisp-civicaddressreportfactory.md) Você pode receber esse objeto por meio [**do evento NewCivicAddressReport.**](newcivicaddressreport.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

