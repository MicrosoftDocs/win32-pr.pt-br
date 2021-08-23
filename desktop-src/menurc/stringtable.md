---
title: Estrutura StringTable
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo membro Children. Uma página de código é um conjunto de caracteres ordenado.
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
ms.openlocfilehash: 01ad7a2436c4b32f0f2fa09ab801339903ed55f35be80bbfc43c4542da4e4ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720656"
---
# <a name="stringtable-structure"></a>Estrutura StringTable

Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo **membro** Children. Uma página de código é um conjunto de caracteres ordenado.

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

Tipo: **WORD**

</dd> <dd>

O comprimento, em bytes, dessa estrutura **StringTable,** incluindo todas as estruturas indicadas pelo **membro** Children.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Esse membro é sempre igual a zero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O tipo de dados no recurso de versão. Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Um número hexadecimal de 8 dígitos armazenado como uma cadeia de caracteres Unicode. Os quatro dígitos mais significativos representam o identificador de idioma. Os quatro dígitos menos significativos representam a página de código para a qual os dados são formatados. Cada identificador de Linguagem Padrão da Microsoft contém duas partes: os 10 bits de ordem baixa especificam o idioma principal e os 6 bits de ordem alta especificam a sublíngua. Para uma tabela de identificadores válidos, consulte .

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Quantas palavras zero necessárias para alinhar o **membro Children** em um limite de 32 bits.

</dd> <dt>

**Filhos**
</dt> <dd>

Tipo: Cadeia **[ **de caracteres**](string-str.md)**

</dd> <dd>

Uma matriz de uma ou mais estruturas [**string.**](string-str.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura de linguagem C verdadeira porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de header fornecidos com o SDK (Software Development Kit) do Windows.

O **membro Children** da estrutura [**StringFileInfo**](stringfileinfo.md) contém pelo menos uma estrutura **StringTable.**

De definir a parte da página de código do membro **szKey** como o valor hexadecimal 0x04b0 para indicar a página de código Unicode ou para o valor hexadecimal da página de código apropriado para o componente de linguagem. Depois de escolher o valor para a página de código, você deve continuar a usar o mesmo valor em revisões posteriores para o arquivo.

Um arquivo executável ou DLL que dá suporte a vários idiomas deve ter um recurso de versão para cada idioma, em vez de um único recurso de versão que contenha cadeias de caracteres em vários idiomas. No entanto, se você usar a estrutura [**Var**](var-str.md) para listar os idiomas compatíveis com seu aplicativo, o número de estruturas **StringTable** no recurso de versão está diretamente relacionado ao número de pares de identificadores de página de código/idioma no membro **Valor** da estrutura **Var.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





