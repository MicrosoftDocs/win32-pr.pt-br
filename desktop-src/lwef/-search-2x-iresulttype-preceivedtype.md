---
title: Propriedade IResultType PreceivedType (WdsSharedIDL.h)
description: Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Propriedade PreceivedType Herdado Windows Recursos de Ambiente
- Propriedade PreceivedType Herdado Windows Recursos de Ambiente, interface IResultType
- Interface IResultType Herdado Windows recursos de ambiente, propriedade PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765a770dc07f1fc0287e861ca79fc2aa941ea7cc425fff29e5e4c5772410c06e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014607"
---
# <a name="iresulttypepreceivedtype-property"></a>Propriedade IResultType::P receivedType

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

retorna o endereço da cadeia de caracteres identifyint do tipo no índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





