---
description: O método FixTimes agrupa os horários de início e parada especificados para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: Método IAMTimelineObj::FixTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6578b18e98c99b471097c98e9dd75de1cdce0c134635cad1fb17e32340eb1a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428416"
---
# <a name="iamtimelineobjfixtimes-method"></a>Método IAMTimelineObj::FixTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método agrupa os horários de início e parada especificados para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo `FixTimes` pai.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início, em unidades de 100 nanossegundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de parada, em unidades de 100 nanossegundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou E \_ NOTINTREE se o objeto não faz parte de um grupo.

## <a name="remarks"></a>Comentários

Durante a renderização, o DES faz a rodada dos horários de início e parada do objeto para o limite de quadro mais próximo. No entanto, o DES não substitui os tempos do objeto. Se você alterar a taxa de quadros de grupo, os tempos arredondados serão sempre calculados com base nos tempos originais. Para obter mais informações, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Use esse método para determinar os horários precisos de início e parada no projeto renderizado. Por exemplo, você deve buscar os horários arredondados, em vez dos horários de início e de parada originais do objeto. Chame [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) para obter os horários originais e passe esses valores para `FixTimes` .

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineObj Interface**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




