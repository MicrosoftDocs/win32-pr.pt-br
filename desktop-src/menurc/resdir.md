---
title: Estrutura RESDIR
description: Contém informações sobre um ícone individual ou componente de cursor em um grupo de recursos. Há uma estrutura RESDIR para cada componente de grupo. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menus de estrutura RESDIR e outros recursos
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105785027"
---
# <a name="resdir-structure"></a>Estrutura RESDIR

Contém informações sobre um ícone individual ou componente de cursor em um grupo de recursos. Há uma estrutura **RESDIR** para cada componente de grupo. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a>Membros

<dl> <dt>

**Ícone**
</dt> <dd>

Tipo: **[ **ICONRESDIR**](iconresdir.md)**

</dd> <dd>

A largura, a altura e a contagem de cores do ícone indicado.

</dd> <dt>

**Cursor**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

A largura e a altura do cursor indicado.

</dd> <dt>

**Aviões**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

O número de planos de cores no bitmap do ícone ou do cursor.

</dd> <dt>

**BitCount**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

O número de bits por pixel no bitmap do ícone ou do cursor.

</dd> <dt>

**BytesInRes**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

O tamanho do recurso, em bytes.

</dd> <dt>

**IconCursorId**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

O ícone ou cursor com um identificador ordinal exclusivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma ou mais estruturas **RESDIR** seguem imediatamente a estrutura [**NEWHEADER**](newheader.md) no arquivo. res. O membro **ResCount** da estrutura **NEWHEADER** especifica o número de estruturas **RESDIR** . Observe que a estrutura **RESDIR** consiste em uma estrutura [**ICONRESDIR**](iconresdir.md) ou uma estrutura [**CURSORDIR**](cursordir.md) seguida pelos membros **aviões**, **BitCount**, **BytesInRes** e **IconCursorId** . Se a estrutura **RESDIR** contiver informações sobre um cursor, as duas **primeiras palavras** do compilador de recursos gravará no recurso de [ \_ cursor de RT](/windows/desktop/menurc/resource-types) são os membros **xHotSpot** e **yHotSpot** da estrutura [**LOCALHEADER**](localheader.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**ICONRESDIR**](iconresdir.md)
</dt> <dt>

[**LOCALHEADER**](localheader.md)
</dt> <dt>

[**NEWHEADER**](newheader.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

