---
title: Estrutura de conalugação
description: Contém um ordinal exclusivo que identifica uma fonte individual no grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menus de estrutura de dialuguel e outros recursos
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644782"
---
# <a name="direntry-structure"></a>Estrutura de conalugação

Contém um ordinal exclusivo que identifica uma fonte individual no grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

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

Tipo: **Word**

</dd> <dd>

Um identificador ordinal exclusivo para uma fonte individual em um grupo de recursos de fonte.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura [**FONTDIRENTRY**](fontdirentry.md) para a fonte especificada segue diretamente a estrutura de **dialuguel** para essa fonte.

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

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





