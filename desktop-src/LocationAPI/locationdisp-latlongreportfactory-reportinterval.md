---
description: O intervalo de eventos de relatório de latitude/longitude atual em milissegundos.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Propriedade LocationDisp. LatLongReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170060"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>Propriedade LocationDisp. LatLongReportFactory. ReportInterval

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

O intervalo de eventos de relatório de latitude/longitude atual em milissegundos.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valor da propriedade

Esta propriedade é um **ULONG** de leitura/gravação.

## <a name="remarks"></a>Comentários

Esse valor é uma solicitação para o provedor de localização. O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado. Leia o valor dessa propriedade para descobrir a configuração real do intervalo de relatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

