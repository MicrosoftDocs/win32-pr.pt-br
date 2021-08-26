---
description: O identificador do índice a ser acessado em um banco de dados.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5711f2927462325b2a6479dd9506099da4bd50f9a9a99b68152e5c0030a47d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001886"
---
# <a name="indexid"></a>INDEXid

O identificador do índice a ser acessado em um banco de dados.


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a>Comentários

Um **IndexID** pode ser um valor inteiro que representa o índice ou o seguinte valor:

<dl> <dt>

<span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXid \_ nulo ((IndexID)-1)
</dt> <dd>

Um **IndexID** inválido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




