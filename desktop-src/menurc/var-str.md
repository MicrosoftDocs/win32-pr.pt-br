---
title: Estrutura de var
description: Representa a organização de dados em um recurso de versão de arquivo. Normalmente, ele contém uma lista de pares de identificadores de página de código e de idioma para os quais a versão do aplicativo ou DLL dá suporte.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menus de estrutura de var e outros recursos
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824771"
---
# <a name="var-structure"></a>Estrutura de var

Representa a organização de dados em um recurso de versão de arquivo. Normalmente, ele contém uma lista de pares de identificadores de página de código e de idioma para os quais a versão do aplicativo ou DLL dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, da estrutura **var** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, do membro de **valor** .

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

A cadeia de caracteres Unicode L "translation".

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palavras zero quantas forem necessárias para alinhar o membro de **valor** em um limite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Uma matriz de um ou mais valores que são pares de identificador de página de código e idioma. Para obter informações adicionais, consulte a seção de comentários a seguir.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.

Se você usar a estrutura **var** para listar os idiomas aos quais seu aplicativo ou DLL dá suporte em vez de usar vários recursos de versão, use o membro **Value** para conter uma matriz de valores **DWORD** indicando as combinações de idioma e página de código com suporte neste arquivo. A palavra de ordem inferior de cada **DWORD** deve conter um identificador de idioma da Microsoft e a palavra de ordem superior deve conter o número da página de código IBM. A palavra de ordem superior ou de ordem inferior pode ser zero, indicando que o arquivo é independente da linguagem ou da página de código. Se a estrutura de **var** for omitida, o arquivo será interpretado como independente da linguagem e da página de código.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





