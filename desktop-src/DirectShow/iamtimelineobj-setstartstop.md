---
description: O método SetStartStop define os horários de início e de parada do objeto, em relação ao pai do objeto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: Método IAMTimelineObj::SetStartStop (Qedit.h)
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
ms.openlocfilehash: e2806d926c9842f5900f46f923f4cbdf8caa47f112e1832077ab7d2b80a9341c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052446"
---
# <a name="iamtimelineobjsetstartstop-method"></a>Método IAMTimelineObj::SetStartStop

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método define os horários de início e parada `SetStartStop` do objeto, em relação ao pai do objeto.

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

Nova hora de início, em unidades de 100 nanossegundos ou –1 para manter a hora de início existente.

</dd> <dt>

*Parar* 
</dt> <dd>

Novo tempo de parada, em unidades de 100 nanossegundos ou –1 para manter a hora de parada existente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                  | Descrição                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Não implementado.<br/>  |



 

## <a name="remarks"></a>Comentários

Faixas, composições e grupos não implementam esse método. Para esses objetos, a hora de início é sempre zero e a hora de parada é o tempo máximo de parada dos objetos que eles contêm.

Não de definir tempos de sobreposição em objetos de origem dentro da mesma faixa. Isso pode causar comportamentos indefinido.

Para objetos de origem, os horários de início e parada são independentes dos horários de início e de parada de mídia. Alterar um par de valores não altera o outro. Para definir os horários de início e parada da mídia, chame o [**método IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Para obter mais informações, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Para obter transições e reduções com precisão de quadro, de definidos os parâmetros *Start* e *Stop* como limites de quadro. Você pode usar o método [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) para converter um valor de tempo no limite de quadro mais próximo ou usar a seguinte função para converter do número de quadro para o tempo de referência:


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

 

 




