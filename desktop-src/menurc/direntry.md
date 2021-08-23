---
title: Estrutura DIRENTRY
description: Contém um ordinal exclusivo que identifica uma fonte individual no grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menus de estrutura DIRENTRY e outros recursos
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 281ede8b2f87e73bf0600d985abd3194a83e8e8f186fa8f780f18f80985e0f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602106"
---
# <a name="direntry-structure"></a>Estrutura DIRENTRY

Contém um ordinal exclusivo que identifica uma fonte individual no grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**fontOrdinal**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Um identificador ordinal exclusivo para uma fonte individual em um grupo de recursos de fonte.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**estrutura FONTDIRENTRY**](fontdirentry.md) para a fonte especificada segue diretamente a estrutura **DIRENTRY** para essa fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





