---
description: 'O método setpositiones define a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: setposicionations.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Método CSourceSeeking. setpositiones (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751887"
---
# <a name="csourceseekingsetpositions-method"></a>Método CSourceSeeking. setpositiones

O `SetPositions` método define a posição atual e a posição de parada. Esse método implementa o método [**IMediaSeeking:: Setposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Ponteiro para uma variável que especifica a posição atual.

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

Combinação bit-a-de de sinalizadores. Consulte Observações.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que especifica a hora de parada, em unidades do formato de hora atual.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Combinação bit-a-de de sinalizadores. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Sucesso<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Sinalizadores inválidos<br/>             |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

Há suporte para os seguintes sinalizadores:

-   Está \_ procurando \_ noposição
-   Estou \_ procurando \_ AbsolutePositioning
-   Estou \_ procurando \_ RelativePositioning
-   Estou \_ procurando \_ IncrementalPositioning (somente *pStop* )

Para obter mais informações, consulte [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Esse método atualiza os valores das variáveis de membro [**CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) e, em seguida, chama os métodos virtuais puros [**CSourceSeeking:: altere**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




