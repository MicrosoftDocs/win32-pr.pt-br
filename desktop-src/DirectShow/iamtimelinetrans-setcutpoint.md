---
description: O método SetCutPoint define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Método IAMTimelineTrans:: SetCutPoint (QEdit. h)'
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
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759908"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>Método IAMTimelineTrans:: SetCutPoint

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetCutPoint` método define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte.

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

Recortar ponto em relação ao início da transição, em unidades de 100 nanossegundos. Se o valor ficar fora dos limites da transição, ele será truncado para a hora válida mais próxima.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Por padrão, o ponto de recorte é o meio da transição. Por exemplo, em uma transição que abrange um segundo, o ponto de recorte padrão é de 0,5 segundos na transição.

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

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




