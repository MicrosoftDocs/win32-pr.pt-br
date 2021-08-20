---
title: Método ResourceLocator.ClearOptions (WSManDisp.h)
description: Remove todas as opções do objeto ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Método ClearOptions Windows Gerenciamento Remoto
- Método ClearOptions Windows gerenciamento remoto, objeto ResourceLocator
- Objeto ResourceLocator Windows Gerenciamento Remoto, Método ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef695b949c62c0d56de45914e1a54996d4d7599f029d136ad78b03ac687365aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112907"
---
# <a name="resourcelocatorclearoptions-method"></a>Método ResourceLocator.ClearOptions

Remove todas as [*opções*](windows-remote-management-glossary.md) do [**objeto ResourceLocator.**](resourcelocator.md) Você pode fornecer um [**objeto ResourceLocator**](resourcelocator.md) em vez [](session.md) de especificar um URI de recurso em operações de objeto session, como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxe


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

**IWSManResourceLocator::ClearOptions** é o método C++ correspondente.

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

 

 





