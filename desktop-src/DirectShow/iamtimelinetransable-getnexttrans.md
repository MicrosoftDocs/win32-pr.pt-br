---
description: O método GetNextTrans recupera a primeira transição que aparece na hora especificada ou posteriormente.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Método IAMTimelineTransable:: GetNextTrans (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761755"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>Método IAMTimelineTransable:: GetNextTrans

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetNextTrans` método recupera a primeira transição que aparece na hora especificada ou posteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppTrans* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de transição.

</dd> <dt>

*Aquecimento* 
</dt> <dd>

Ponteiro para uma variável que especifica a hora em unidades de 100 a nanossegundos. Na entrada, esse valor especifica a hora a partir da qual encontrar a transição. Na saída, se uma transição for recuperada, esse valor será definido como a hora de parada da transição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o método recuperar uma transição ou S \_ false se não encontrar uma transição. Caso contrário, retorna um valor **HRESULT** que indica a causa da falha.

## <a name="remarks"></a>Comentários

A hora de início da transição pode ser menor que a hora especificada em *pinagem*, se a transição abranger o tempo especificado.

Se o método retornar S \_ OK, a interface [**IAMTimelineObj**](iamtimelineobj.md) que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




