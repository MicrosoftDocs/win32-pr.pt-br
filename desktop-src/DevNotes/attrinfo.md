---
description: Contém os dados de atributo de um arquivo.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Estrutura ATTRINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826128"
---
# <a name="attrinfo-structure"></a>Estrutura ATTRINFO

Contém os dados de atributo de um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**tAttrID**
</dt> <dd>

O tipo de atributo. Consulte [tipos de marca](tag-types.md).

</dd> <dt>

**dwFlags**
</dt> <dd>

Os sinalizadores para este atributo.



| Valor                                                                                                                                                                                                                                           | Significado                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**Atributo \_ DISPONÍVEL**</dt> <dt>0x00000001</dt> </dl> | O atributo está disponível.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**Atributo \_ FALHA**</dt> de <dt>0x00000002</dt> </dl>          | A chamada falhou porque o atributo não está disponível.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Um valor **QWORD** (se o tipo de marca for **marca \_ tipo \_ QWORD**).

</dd> <dt>

**dwAttr**
</dt> <dd>

Um valor **DWORD** (se o tipo de marca for **marca \_ tipo \_ DWORD**).

</dd> <dt>

**lpAttr**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres (se o tipo de marca for **tipo de marca \_ \_ STRINGREF**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




