---
description: Armazena informações sobre tipos de link e é usada pela interface IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Estrutura LINKINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164338"
---
# <a name="linkinfo-structure"></a>Estrutura LINKINFO

\[Só há suporte para **LINKINFO** e [**IITEMPREVIEWEREXT**](-search-iitempreviewerext.md) no Windows XP e no Windows Server 2003 e não deve mais ser usado.\]

Armazena informações sobre tipos de link e é usada pela interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**tipo**
</dt> <dd>

Tipo: **[ **LinkId**](-search-linktype.md)**

</dd> <dd>

O tipo de link especificado ao rastrear ou indexar indicado por uma constante de [**LinkId**](-search-linktype.md) .

</dd> <dt>

**bstrContentType**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um valor **BSTR** que especifica o tipo de conteúdo.

</dd> <dt>

**bstrEncoding**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um atributo encodingStyle especificado no arquivo WSDL (Web Services Description Language).

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um valor **BSTR** que especifica a extensão de nome de arquivo.

</dd> <dt>

**varData**
</dt> <dd>

Tipo: **variante**

</dd> <dd>

Uma variante que especifica o valor da variável.

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Um **DWORD** que especifica as partes relacionadas.

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um valor **BSTR** que especifica uma propriedade CID, uma cadeia de caracteres decimal assinada não preenchida.

</dd> <dt>

**lCodePage**
</dt> <dd>

Tipo: **longo**

</dd> <dd>

A página de código a ser usada para codificar a cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a estrutura **LINKINFO** e as seguintes APIs: os métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 




