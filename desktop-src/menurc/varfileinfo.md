---
title: Estrutura VarFileInfo
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão não dependentes de uma combinação de linguagem de código e de idioma específico.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menus de estrutura VarFileInfo e outros recursos
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790309"
---
# <a name="varfileinfo-structure"></a>Estrutura VarFileInfo

Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão não dependentes de uma combinação de linguagem de código e de idioma específico.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, do bloco **VarFileInfo** inteiro, incluindo todas as estruturas indicadas pelo membro **filho** .

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

A cadeia de caracteres Unicode L "VarFileInfo".

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.

</dd> <dt>

**Filhos**
</dt> <dd>

Tipo: **[ **var**](var-str.md)**

</dd> <dd>

Normalmente contém uma lista de idiomas aos quais o aplicativo ou DLL dá suporte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.

O membro **filho** da estrutura do [**vs \_ VERSIONINFO**](vs-versioninfo.md) pode conter zero ou um **VarFileInfo** estruturas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





