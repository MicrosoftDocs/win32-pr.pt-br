---
description: Define maneiras de mapear para uma ID de classe.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Enumeração TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: 15e7ecdc06495c0fa68b2949ae159bbc76b8cababd2b8703d3ebbdebb874399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075750"
---
# <a name="tyspec-enumeration"></a>Enumeração TYSPEC

Define maneiras de mapear para uma ID de classe.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**
</dt> <dd>

UM CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**
</dt> <dd>

Uma extensão de nome de arquivo. Não há suporte para esse valor no momento.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**\_MIMETYPE TYSPEC**
</dt> <dd>

Um tipo MIME. Não há suporte para esse valor no momento.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nome de arquivo TYSPEC**
</dt> <dd>

Um nome de arquivo. Não há suporte para esse valor no momento.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**ProgID do TYSPEC \_**
</dt> <dd>

UM PROGID. Não há suporte para esse valor no momento.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PackageName**
</dt> <dd>

Um nome de pacote. Não há suporte para esse valor no momento.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_OBJECTID TYSPEC**
</dt> <dd>

Uma ID do objeto. Não há suporte para esse valor no momento.

</dd> </dl>

## <a name="remarks"></a>Comentários

A União **uCLSSPEC** é definida da seguinte maneira:

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>Wtypes. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instalar**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
