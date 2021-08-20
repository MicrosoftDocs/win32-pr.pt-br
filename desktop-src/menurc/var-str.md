---
title: Estrutura var
description: Representa a organização de dados em um recurso de versão de arquivo. Normalmente, ele contém uma lista de pares de identificadores de página de código e idioma compatíveis com a versão do aplicativo ou DLL.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menus de estrutura var e outros recursos
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48537009b56d2b37f4508871049463a65a12965c31658e932716832955503f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599576"
---
# <a name="var-structure"></a>Estrutura var

Representa a organização de dados em um recurso de versão de arquivo. Normalmente, ele contém uma lista de pares de identificadores de página de código e idioma compatíveis com a versão do aplicativo ou DLL.

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

Tipo: **WORD**

</dd> <dd>

O comprimento, em bytes, da **estrutura Var.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O comprimento, em bytes, do **membro** Value.

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

A cadeia de caracteres Unicode L"Translation".

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Quantas palavras zero necessárias para alinhar o **membro Value** em um limite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Uma matriz de um ou mais valores que são pares de identificador de página de código e idioma. Para obter informações adicionais, consulte a seção Comentários a seguir.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura de linguagem C verdadeira porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de header fornecidos com o SDK (Software Development Kit) do Windows.

Se você usar a estrutura **Var** para listar os idiomas compatíveis com seu aplicativo ou DLL em vez de usar vários recursos de versão, use o membro **Value** para conter uma matriz de valores **DWORD** indicando as combinações de idioma e página de código compatíveis com esse arquivo. A palavra de ordem baixa de cada **DWORD** deve conter um identificador de idioma da Microsoft e a palavra de ordem alta deve conter o número da página de código IBM. A palavra de ordem alta ou baixa pode ser zero, indicando que o arquivo é independente de idioma ou página de código. Se a **estrutura Var** for omitida, o arquivo será interpretado como independente de página de código e idioma.

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

[**Stringtable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





