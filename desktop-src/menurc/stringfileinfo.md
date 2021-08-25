---
title: Estrutura StringFileInfo
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão que podem ser exibidas para uma determinada linguagem e página de código.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menus de estrutura StringFileInfo e outros recursos
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e130090c7281f6ef61ed0a3a82b822863bb5c12ff1194e26b07a70467db82cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720826"
---
# <a name="stringfileinfo-structure"></a>Estrutura StringFileInfo

Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão que podem ser exibidas para uma determinada linguagem e página de código.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, do bloco **StringFileInfo** inteiro, incluindo todas as estruturas indicadas pelo membro **filho** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Esse membro é sempre igual a zero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tipo de dados no recurso de versão. Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

A cadeia de caracteres Unicode L "StringFileInfo".

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.

</dd> <dt>

**Filhos**
</dt> <dd>

Tipo: **[ **STRINGTABLE**](stringtable.md)**

</dd> <dd>

Uma matriz de uma ou mais estruturas [**STRINGTABLE**](stringtable.md) . Cada membro **szKey** da estrutura **STRINGTABLE** indica o idioma e a página de código apropriados para exibir o texto nessa estrutura **STRINGTABLE** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável. essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) Windows.

O membro **filho** da estrutura do [**vs \_ VERSIONINFO**](vs-versioninfo.md) pode conter zero ou mais estruturas **StringFileInfo** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





