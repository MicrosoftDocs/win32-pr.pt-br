---
title: Propriedade PropertyCount IResultType (WdsSharedIDL.h)
description: Essa propriedade contém o número de propriedades expostas pelo tipo.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Propriedade PropertyCount Herdou Windows recursos de ambiente
- Propriedade PropertyCount Recursos Windows ambiente herdado, interface IResultType
- Interface IResultType Recursos Windows ambiente herdado, propriedade PropertyCount
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6952f2efb6e0d14be22daf71e352747915b2ba05bf543d764ee9af5f496715ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014626"
---
# <a name="iresulttypepropertycount-property"></a>Propriedade IResultType::P ropertyCount

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Essa propriedade contém o número de propriedades expostas pelo tipo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor da propriedade

retorna o endereço do número de propriedades expostas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





