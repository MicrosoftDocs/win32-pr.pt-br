---
description: O método SetStartStop define as horas de início e de parada do objeto, em relação ao pai do objeto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Método IAMTimelineObj:: SetStartStop (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760087"
---
# <a name="iamtimelineobjsetstartstop-method"></a>Método IAMTimelineObj:: SetStartStop

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetStartStop` método define as horas de início e de parada do objeto, em relação ao pai do objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Nova hora de início, em unidades de 100 a nanossegundos ou – 1 para manter a hora de início existente.

</dd> <dt>

*Parar* 
</dt> <dd>

Nova hora de parada, em unidades de 100 a nanossegundos ou – 1 para manter a hora de parada existente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                  | Descrição                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Não implementado.<br/>  |



 

## <a name="remarks"></a>Comentários

Faixas, composições e grupos não implementam esse método. Para esses objetos, a hora de início é sempre zero e a hora de parada é a hora de término máxima dos objetos que eles contêm.

Não defina os horários sobrepostos em objetos de origem dentro da mesma faixa. Isso pode causar comportamentos indefinidos.

Para os objetos de origem, os horários de início e de parada são independentes das horas de início e de parada de mídia. A alteração de um par de valores não altera o outro. Para definir os horários de início e de parada da mídia, chame o método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).

Para obter cortes e transições com precisão de quadro, defina os parâmetros *Iniciar* e *parar* como limites de quadro. Você pode usar o método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) para converter um valor de hora no limite de quadro mais próximo ou usar a seguinte função para converter de número de quadro em tempo de referência:


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



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

 

 




