---
description: Nome do PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Membro CBasePin:: m_pName (Amfilter. h)'
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
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751706"
---
# <a name="cbasepinm_pname-member"></a>Membro de CBasePin:: m \_ pname

Nome do PIN.

## <a name="syntax"></a>Sintaxe


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Comentários

O método [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md) retorna essa cadeia de caracteres como o nome do PIN e o método [**CBasePin:: QueryId**](cbasepin-queryid.md) o retorna como o identificador do PIN. Em geral, no entanto, o nome do PIN e o identificador do PIN não precisam ser os mesmos. O identificador de PIN é usado para persistência de gráfico. Para obter mais informações, consulte [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




