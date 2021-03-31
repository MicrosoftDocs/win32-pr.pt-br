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
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369488"
---
# <a name="istorageprovidercopyhook-interface"></a>Interface IStorageProviderCopyHook

Expõe um método que determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.

## <a name="members"></a>Membros

A interface **IStorageProviderCopyHook** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IStorageProviderCopyHook** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IStorageProviderCopyHook** tem esses métodos.



| Método                                           | Descrição                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.                                                           |


## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Build 19624 do Windows 10 Insider Preview                                                |
| parâmetro<br/>                   | ShObjIdl. h   |
