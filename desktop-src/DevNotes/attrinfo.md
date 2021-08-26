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
ms.openlocfilehash: 090f2ab58d8bf1eb4e379166086d31389b533712a3df23f987bba1331f990891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103726"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




