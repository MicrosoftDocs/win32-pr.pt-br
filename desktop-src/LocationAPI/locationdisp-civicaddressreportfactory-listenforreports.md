---
description: Solicita eventos de relatório de endereços cívicos.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Método LocationDisp. CivicAddressReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 218684dcdb1c79b3b1a37517a4369ad492031cae1badfb9f0b16bbb6933289d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979766"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>Método LocationDisp. CivicAddressReportFactory. ListenForReports

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use o [**Windows. API de dispositivos. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Solicita eventos de relatório de endereços cívicos.

## <a name="syntax"></a>Sintaxe


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Número (**palavra dupla**) que representa o tempo solicitado entre eventos de relatório de endereço cívico, em milissegundos. Consulte Observações.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O provedor de localização não é necessário para fornecer a precisão solicitada. Leia o valor da propriedade [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) para descobrir a configuração real do intervalo de relatório.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [escutando eventos de relatório de endereço cívico](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento NewCivicAddressReport**](newcivicaddressreport.md)
</dt> </dl>

 

