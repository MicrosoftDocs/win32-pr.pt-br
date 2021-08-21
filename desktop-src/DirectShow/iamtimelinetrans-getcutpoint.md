---
description: O método GetCutPoint recupera o ponto de recorte.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Método IAMTimelineTrans:: GetCutPoint (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0582446a3f88b3692b50ca97d033a85d1dfca475051e3538c39d41003e788ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154790"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>Método IAMTimelineTrans:: GetCutPoint

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetCutPoint` método recupera o ponto de recorte. Se você renderizar uma transição como um recorte, o ponto de recorte é o horário em que a transição é recortada de uma origem para a outra. Por padrão, esse valor é o meio da transição. Por exemplo, em uma transição que abrange um segundo, o ponto de recorte padrão é de 0,5 segundos na transição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTLTime* 
</dt> <dd>

Recebe o ponto de recorte, em relação à hora de início da transição, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                               | Descrição                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>   | O ponto de recorte não foi definido. O valor retornado é o valor padrão.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | O ponto de recorte foi definido com um valor diferente do padrão.<br/>            |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/>                                          |



 

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

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutsOnly**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




