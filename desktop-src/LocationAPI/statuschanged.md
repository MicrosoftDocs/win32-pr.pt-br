---
description: Ocorre quando o status operacional de um relatório é alterado.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Evento StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172341"
---
# <a name="statuschanged-event"></a>Evento StatusChanged

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Ocorre quando o status operacional de um relatório é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*status* 
</dt> <dd>

O novo status.



| Status                                                                                               | Significado                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Relatório sem suporte.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erro.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Acesso negado.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Running.<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Você deve implementar manipuladores de relatório de alteração de status separados para relatórios de endereço cívico e relatórios de latitude/longitude.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse evento, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

