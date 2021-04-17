---
description: Número de threads de streaming usando este pin.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Membro CDynamicOutputPin:: m_dwNumOutstandingOutputPinUsers (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787409"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>Membro de CDynamicOutputPin:: m \_ dwNumOutstandingOutputPinUsers

Número de threads de streaming usando este pin.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Comentários

O método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa essa variável e o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) a decrementa. Quando o valor for maior que zero, algum thread usará esse PIN para transmitir dados ou para alterar o tipo de conexão. O PIN não pode ser bloqueado enquanto este for o caso.

Antes de acessar essa variável, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




