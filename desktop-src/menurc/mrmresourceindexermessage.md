---
title: Estrutura MrmResourceIndexerMessage (MrmResourceIndexer. h)
description: Representa uma mensagem gerada por um indexador de recurso. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Menus de estrutura MrmResourceIndexerMessage e outros recursos
- Menus de ponteiro de estrutura PMrmResourceIndexerMessage e outros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessage
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073c4f74852d341d7f0711a34abe4459dcbaa79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918126"
---
# <a name="mrmresourceindexermessage-structure"></a>Estrutura MrmResourceIndexerMessage

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Representa uma mensagem gerada por um indexador de recurso. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MrmResourceIndexerMessage {
  MrmResourceIndexerMessageSeverity severity;
  ULONG                             id;
  PCWSTR                            text;
} MrmResourceIndexerMessage, *PMrmResourceIndexerMessage;
```



## <a name="members"></a>Membros

<dl> <dt>

**severity**
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)**

</dd> <dd>

Um valor que indica a severidade da mensagem.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **ULONG**

</dd> <dd>

Um identificador exclusivo para a mensagem.

</dd> <dt>

**text**
</dt> <dd>

Tipo: **PCWSTR**

</dd> <dd>

O texto da mensagem. Não libere esse ponteiro; a memória pertence ao sistema operacional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

