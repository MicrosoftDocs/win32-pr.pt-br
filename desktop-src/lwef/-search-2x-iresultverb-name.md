---
title: Propriedade Nome de IResultVerb (WdsSharedIDL.h)
description: Essa propriedade retorna um ponteiro para o nome conódico para o verbo, como print, open, etc.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Propriedade name Legacy Windows Environment Features
- Propriedade name Legacy Windows Environment Features , interface IResultVerb
- Interface IResultVerb Recursos Windows ambiente herdado, propriedade Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e58377a9286a6e3fe4abb8d0a1d4ebf9e10bd3072295484ca32fb56d465a6f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976966"
---
# <a name="iresultverbname-property"></a>Propriedade IResultVerb::Name

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Essa propriedade retorna um ponteiro para o nome conódico para o verbo, como print, open, etc.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

name é um ponteiro para o nome conódico do verbo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





