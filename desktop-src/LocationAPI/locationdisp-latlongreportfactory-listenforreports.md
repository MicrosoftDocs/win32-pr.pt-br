---
description: Solicita eventos de relatório de latitude/longitude.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Método LocationDisp. LatLongReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662434"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a>Método LocationDisp. LatLongReportFactory. ListenForReports

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Solicita eventos de relatório de latitude/longitude.

## <a name="syntax"></a>Sintaxe


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Número (**palavra dupla**) que representa o tempo solicitado entre os eventos de relatório de latitude/longitude, em milissegundos. Consulte Observações.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado. Leia o valor da propriedade [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) para descobrir a configuração real do intervalo de relatório.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| parâmetro<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



 

