---
description: 'O método SetCutPoint2 define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte. Esse método é equivalente a IAMTimelineTrans:: SetCutPoint, mas usa um valor de REFTIME.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Método IAMTimelineTrans:: SetCutPoint2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9d4dedfb31efab45f56229e2dd4db10fc9e43defe822662bc2d7be06f0c1a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502336"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>Método IAMTimelineTrans:: SetCutPoint2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetCutPoint2` método define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte. Esse método é equivalente a [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md), mas usa um valor de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TLTime* 
</dt> <dd>

Recortar ponto em relação ao início da transição, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




