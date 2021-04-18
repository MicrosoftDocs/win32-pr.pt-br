---
title: Estrutura StringTable
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo membro filho. Uma página de código é um conjunto de caracteres ordenados.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menus de estrutura StringTable e outros recursos
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369357"
---
# <a name="stringtable-structure"></a>Estrutura StringTable

Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo membro **filho** . Uma página de código é um conjunto de caracteres ordenados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, dessa estrutura **STRINGTABLE** , incluindo todas as estruturas indicadas pelo membro **filho** .

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

Um número hexadecimal de 8 dígitos armazenado como uma cadeia de caracteres Unicode. Os quatro dígitos mais significativos representam o identificador de idioma. Os quatro dígitos menos significativos representam a página de código para a qual os dados são formatados. Cada identificador de idioma padrão da Microsoft contém duas partes: os 10 bits de ordem inferior especificam o idioma principal e os 6 bits de ordem superior especificam o subidioma. Para obter uma tabela de identificadores válidos, consulte.

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.

</dd> <dt>

**Filhos**
</dt> <dd>

Tipo: **[ **cadeia de caracteres**](string-str.md)**

</dd> <dd>

Uma matriz de uma ou mais estruturas de [**cadeia de caracteres**](string-str.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.

O membro **filho** da estrutura [**StringFileInfo**](stringfileinfo.md) contém pelo menos uma estrutura **STRINGTABLE** .

Defina a parte da página de código do membro **szKey** como o valor hexadecimal 0x04b0 para indicar a página de código Unicode ou para o valor hexadecimal da página de código apropriada para o componente de linguagem. Depois de escolher o valor para a página de código, você deve continuar a usar o mesmo valor em revisões posteriores para o arquivo.

Um arquivo executável ou DLL que dá suporte a vários idiomas deve ter um recurso de versão para cada idioma, em vez de um único recurso de versão que contém cadeias de caracteres em vários idiomas. No entanto, se você usar a estrutura [**var**](var-str.md) para listar os idiomas aos quais seu aplicativo dá suporte, o número de estruturas **STRINGTABLE** no recurso de versão estará diretamente relacionado ao número de pares de identificador de página de código/idioma no membro de **valor** da estrutura **var** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Strings**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





