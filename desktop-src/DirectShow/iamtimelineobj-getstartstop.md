---
description: O método GetStartStop recupera os horários de início e parada do objeto, em relação ao pai do objeto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: Método IAMTimelineObj::GetStartStop (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400782"
---
# <a name="iamtimelineobjgetstartstop-method"></a>Método IAMTimelineObj::GetStartStop

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método recupera os horários de início e parada do objeto, em relação ao `GetStartStop` pai do objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Recebe a hora de início, em unidades de 100 nanossegundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recebe o tempo de parada, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

As composições, grupos e faixas sempre têm uma hora de início de 0.

Durante a renderização, o DES faz a rodada dos horários de início e parada de um objeto para o limite de quadro mais próximo. No entanto, o DES não substitui os tempos do objeto. Se você alterar a taxa de quadros de grupo, os tempos arredondados serão sempre calculados com base nos tempos originais. Para obter mais informações, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Para determinar os horários de início e parada no projeto renderizado, passe os valores retornados por para o `GetStartStop` [**método IAMTimelineObj::FixTimes.**](iamtimelineobj-fixtimes.md)

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

 

 




