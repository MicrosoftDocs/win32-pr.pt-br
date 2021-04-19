---
title: Estrutura de TF_RENDERINGMARKUP
description: A \_ estrutura de estrutura TF RENDERINGMARKUP contém um intervalo e as informações de atributo de exibição.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Estrutura de serviços de texto do TF_RENDERINGMARKUP Structure
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105813075"
---
# <a name="tf_renderingmarkup-structure"></a>Estrutura de RENDERINGMARKUP de TF \_

A estrutura de estrutura [**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contém um intervalo e as informações de atributo de exibição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Membros

<dl> <dt>

**pRange**
</dt> <dd>

Um ponteiro para uma interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .

</dd> <dt>

**tfDisplayAttr**
</dt> <dd>

Exibir informações de atributo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 




