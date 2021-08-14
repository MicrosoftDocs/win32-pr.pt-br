---
description: Ocorre quando um novo relatório de endereço civil é gerado.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Evento NewCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 61b5c6c05d8aa551148d278fa0cbafa8791bbc4c1a1f6b1142ef7f2ef80af318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386701"
---
# <a name="newcivicaddressreport-event"></a>Evento NewCivicAddressReport

\[O modelo de objeto da API de Localização está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de Geolocalização do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo da área de trabalho, use o [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Ocorre quando um novo relatório de endereço civil é gerado.

## <a name="syntax"></a>Sintaxe


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newReport* 
</dt> <dd>

O novo [**objeto LocationDisp.DispCivicAddressReport.**](locationdisp-dispcivicaddressreport.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="examples"></a>Exemplos

Para ver um exemplo de como usar esse evento, consulte [Escutando eventos de relatório de endereço](/uwp/api/Windows.Devices.Geolocation)civil.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

