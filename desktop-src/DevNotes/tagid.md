---
description: Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4c65183170c7304bf05a670b1eadb3a5953d6f33b1f6415210f12db8898760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075772"
---
# <a name="tagid"></a>TAGID

Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Comentários

Um **TagId** é específico para um banco de dados. Pode ser um valor inteiro que representa o índice ou um dos seguintes valores:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ nulo (0)
</dt> <dd>

O **TagId** não existe. Esse valor é retornado de uma função quando não pode retornar um **TagId** válido.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Raiz TagId (0)
</dt> <dd>

Indica uma marca de lista raiz que pode ser usada como um pai para obter um **TagId** filho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tags**](tag.md)
</dt> <dt>

[Tipos de marca](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




