---
title: Estrutura CURSORDIR
description: Contém as dimensões de uma imagem de cursor individual em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menus de estrutura CURSORDIR e outros recursos
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7194d6af764a9f66a2bf1a059f9c387cde13bb05728a7e96ccec470fa3650c81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602166"
---
# <a name="cursordir-structure"></a>Estrutura CURSORDIR

Contém as dimensões de uma imagem de cursor individual em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A largura do cursor, em pixels. Os valores aceitáveis são 16, 32 e 64.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A altura do cursor, em pixels. Os valores aceitáveis são 16, 32 e 64.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **CURSORDIR** é passada na estrutura [**RESDIR**](resdir.md) se a estrutura **RESDIR** descreve um cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





