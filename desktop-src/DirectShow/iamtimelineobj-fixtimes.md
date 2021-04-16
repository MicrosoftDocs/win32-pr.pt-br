---
description: O método FixTimes arredonda as horas de início e de término especificadas para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Método IAMTimelineObj:: FixTimes (QEdit. h)'
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
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758062"
---
# <a name="iamtimelineobjfixtimes-method"></a>Método IAMTimelineObj:: FixTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `FixTimes` método arredonda as horas de início e de término especificadas para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início, em unidades de 100 a nanossegundos. Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de parada, em unidades de 100 a nanossegundos. Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido, ou E \_ NOTINTREE se o objeto não fizer parte de um grupo.

## <a name="remarks"></a>Comentários

Durante a renderização, o DES arredonda as horas de início e de parada do objeto para o limite de quadro mais próximo. No entanto, o DES não substitui os horários do objeto. Se você alterar a taxa de quadros do grupo, os horários arredondados serão sempre calculados a partir dos horários originais. Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).

Use esse método para determinar os horários de início e de parada precisos no projeto renderizado. Por exemplo, você deve procurar os horários arredondados, em vez de os horários de início e de término originais do objeto. Chame [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md) para obter os horários originais e passe esses valores para `FixTimes` .

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




