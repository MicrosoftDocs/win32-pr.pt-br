---
description: Define um método que determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.
title: Interface IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: aa26a329bd80295a6a46a1bb11d1dc651baf1ea71975576ed704b29a7fee8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968865"
---
# <a name="istorageprovidercopyhook-interface"></a>Interface IStorageProviderCopyHook

Expõe um método que determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.

## <a name="members"></a>Membros

A interface **IStorageProviderCopyHook** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IStorageProviderCopyHook** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IStorageProviderCopyHook** tem esses métodos.



| Método                                           | Descrição                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.                                                           |


## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 10 Insider Preview Build 19624                                                |
| Cabeçalho<br/>                   | shobjidl.h   |
