---
description: O método GetNextVTrack recupera a próxima faixa virtual após uma faixa virtual especificada.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Método IAMTimelineComp:: GetNextVTrack (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785344"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>Método IAMTimelineComp:: GetNextVTrack

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetNextVTrack` método recupera a próxima faixa virtual após uma faixa virtual especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Ponteiro para o controle virtual anterior ou **NULL** para recuperar a primeira faixa virtual na composição.

</dd> <dt>

*ppNextVirtualTrack* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do próximo controle virtual, em ordem de prioridade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o método recuperar uma faixa virtual ou, \_ caso contrário, false.

## <a name="remarks"></a>Comentários

Se o método for executado com sucesso, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




