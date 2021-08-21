---
title: Método ResourceLocator.ClearSelectors (WSManDisp.h)
description: Remove todos os seletores de um objeto ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Método ClearSelectors Windows Gerenciamento Remoto
- Método ClearSelectors Windows gerenciamento remoto, objeto ResourceLocator
- Objeto ResourceLocator Windows Gerenciamento Remoto, método ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54fda16aa67086304e62b4c762769cc7dea832437a939f3928eda665623f5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112829"
---
# <a name="resourcelocatorclearselectors-method"></a>Método ResourceLocator.ClearSelectors

Remove todos os [*seletores de*](windows-remote-management-glossary.md) um [**objeto ResourceLocator.**](resourcelocator.md) Você pode fornecer um [**objeto ResourceLocator**](resourcelocator.md) em vez [](session.md) de especificar um URI de recurso em operações de objeto session, como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxe


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

**IWSManResourceLocator::ClearSelectors** é o método C++ correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 





