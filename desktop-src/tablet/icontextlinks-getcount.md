---
description: Obtém o número de objetos IContextLink nesta coleção.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'Método IContextLinks:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164548"
---
# <a name="icontextlinksgetcount-method"></a>Método IContextLinks:: GetCount

Obtém o número de objetos [**IContextLink**](icontextlink.md) nesta coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulCount* \[ out, retval\]
</dt> <dd>

O número de objetos [**IContextLink**](icontextlink.md) contidos nesta coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




