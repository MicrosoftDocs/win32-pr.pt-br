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
ms.openlocfilehash: d594ae41109e072413e20709c68770038fbae870966325f762ddd169900491d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874199"
---
# <a name="tf_renderingmarkup-structure"></a>Estrutura de RENDERINGMARKUP de TF \_

A estrutura de estrutura [**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contém um intervalo e as informações de atributo de exibição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ITfRange*           pRange;
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

 

 




