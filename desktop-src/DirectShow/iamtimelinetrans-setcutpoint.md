---
description: O método SetCutPoint define a hora em que a transição é cortada de uma fonte para a próxima, se a transição for renderizada como um corte.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: Método IAMTimelineTrans::SetCutPoint (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c411925ebe10ad35641e38ae2332605d7691ae24f0cc96ff716bd7d00e6603f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052066"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>Método IAMTimelineTrans::SetCutPoint

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método define a hora em que a transição é cortada de uma fonte para a próxima, se a transição `SetCutPoint` for renderizada como um corte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TLTime* 
</dt> <dd>

Ponto de corte relativo ao início da transição, em unidades de 100 nanossegundos. Se o valor estiver fora dos limites da transição, ele será truncado para a hora válida mais próxima.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Por padrão, o ponto de corte é o meio da transição. Por exemplo, em uma transição que abrange um segundo, o ponto de corte padrão é de 0,5 segundo para a transição.

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

[**IAMTimelineTrans Interface**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




