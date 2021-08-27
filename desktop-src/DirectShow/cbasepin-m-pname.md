---
description: Nome do pino.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: Membro CBasePin::m_pName (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052676"
---
# <a name="cbasepinm_pname-member"></a>Membro CBasePin::m \_ pName

Nome do pino.

## <a name="syntax"></a>Sintaxe


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Comentários

O [**método CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) retorna essa cadeia de caracteres como o nome do pino e o [**método CBasePin::QueryId**](cbasepin-queryid.md) a retorna como o identificador de pino. Em geral, no entanto, o nome do pino e o identificador de pino não precisam ser os mesmos. O identificador de pino é usado para persistência de grafo. Para obter mais informações, consulte [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




