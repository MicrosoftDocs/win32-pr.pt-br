---
description: O intervalo de eventos do relatório de endereço civil atual em milissegundos.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Propriedade LocationDisp.CivicAddressReportFactory.ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387157"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Propriedade LocationDisp.CivicAddressReportFactory.ReportInterval

\[O modelo de objeto da API de Localização está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de Geolocalização do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo da área de trabalho, use o [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

O intervalo de eventos do relatório de endereço civil atual em milissegundos.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade é um **ULONG de leitura/gravação.**

## <a name="remarks"></a>Comentários

Esse valor é uma solicitação para o provedor de localização. O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado. Leia o valor dessa propriedade para descobrir a configuração de intervalo de relatório verdadeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

