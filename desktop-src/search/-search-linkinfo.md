---
description: Armazena informações sobre tipos de link e é usado pela interface IItemPreviewerExt.
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
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863939"
---
# <a name="linkinfo-structure"></a>Estrutura LINKINFO

\[**LINKINFO** e [**IItemPreviewerExt**](-search-iitempreviewerext.md) têm suporte apenas no Windows XP e Windows Server 2003 e não devem mais ser usados.\]

Armazena informações sobre tipos de link e é usado pela interface [**IItemPreviewerExt.**](-search-iitempreviewerext.md)

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

Tipo: **[ **LINKTYPE**](-search-linktype.md)**

</dd> <dd>

O tipo de link especificado ao rastrear ou indexar indicado por uma [**constante LINKTYPE.**](-search-linktype.md)

</dd> <dt>

**bstrContentType**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um **valor BSTR** que especifica o tipo de conteúdo.

</dd> <dt>

**bstrEncoding**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um atributo EncodingStyle especificado no arquivo WSDL (Linguagem de Descrição dos Serviços Web).

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Um **valor BSTR** que especifica a extensão de nome de arquivo.

</dd> <dt>

**varData**
</dt> <dd>

Tipo: **VARIANT**

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

Um **valor BSTR** que especifica uma propriedade Cid, uma cadeia de caracteres decimal assinada não com preenchimento.

</dd> <dt>

**lCodePage**
</dt> <dd>

Tipo: **Longo**

</dd> <dd>

A página de código a ser usada para codificar a cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para visualizar anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a estrutura **LINKINFO** e as seguintes APIs: os métodos [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e a enumeração [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>          |



 

 




