---
description: TAGREF – contém o índice de uma entrada e suas informações de TAG em um banco de dados shim.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5a9de8da025e8278ab0bca7ccbe16d70d16b782591181f6ce6ce74a010a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075770"
---
# <a name="tagref"></a>TAGREF

Contém o índice de uma entrada e suas informações de TAG em um banco de dados shim.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Comentários

Um **TAGREF é específico** para um banco de dados shim e válido em vários bancos de dados. Pode ser um valor inteiro que representa o índice ou um dos seguintes valores:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)
</dt> <dd>

O **TAGREF** não existe. Esse valor é retornado de uma função quando não pode retornar um **TAGREF válido.**

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)
</dt> <dd>

Indica uma TAG de lista raiz que pode ser usada como um pai para obter um **TAGREF filho.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**Tag**](tag.md)
</dt> <dt>

[Tipos de TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




