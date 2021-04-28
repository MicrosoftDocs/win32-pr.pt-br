---
description: TAGREF-contém o índice de uma entrada e suas informações de marca em um banco de dados de Shim.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096624"
---
# <a name="tagref"></a>TAGREF

Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Comentários

Um **TAGREF** é específico para um banco de dados de Shim e é válido em vários bancos. Pode ser um valor inteiro que representa o índice ou um dos seguintes valores:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ nulo (0)
</dt> <dd>

O **TAGREF** não existe. Esse valor é retornado de uma função quando não pode retornar um **TAGREF** válido.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Raiz TAGREF (0)
</dt> <dd>

Indica uma marca de lista raiz que pode ser usada como um pai para obter um **TAGREF** filho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**Tags**](tag.md)
</dt> <dt>

[Tipos de marca](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




