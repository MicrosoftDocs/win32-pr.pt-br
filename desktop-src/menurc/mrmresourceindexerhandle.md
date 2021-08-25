---
title: Estrutura MrmResourceIndexerHandle (MrmResourceIndexer.h)
description: Representa um identificador opaco para um objeto de indexador de recursos. O handle é gerenciado pelo sistema operacional. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de build personalizados.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menus de estrutura MrmResourceIndexerHandle e outros recursos
- Menus de ponteiro de estrutura PMrmResourceIndexerHandle e outros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c9cd18d6c828d5f9b5187f866d8ab637dfd4d58c3da0a8569bd8c910c7e872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825686"
---
# <a name="mrmresourceindexerhandle-structure"></a>Estrutura MrmResourceIndexerHandle

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Representa um identificador opaco para um objeto de indexador de recursos. O handle é gerenciado pelo sistema operacional. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a>Membros

<dl> <dt>

**Lidar com**
</dt> <dd>

Tipo: **PVOID**

</dd> <dd>

Um identificador opaco para um objeto de indexador de recursos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do servidor\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

