---
description: O método pause pausa o filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Método CBaseRenderer. PAUSE (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769238"
---
# <a name="cbaserendererpause-method"></a>Método CBaseRenderer. Pause

O `Pause` método pausa o filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                             | Descrição                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | A transição foi concluída.<br/> |
| <dl> <dt>**\_falso**</dt> </dl> | A transição não foi concluída.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseFilter::P ause**](cbasefilter-pause.md) . Ele executa as seguintes etapas:

-   Chama o método **CBaseFilter::P ause** .
-   Confirma o alocador. (Consulte [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Se o estado anterior foi interrompido, o filtro libera qualquer amostra que está segurando. (O exemplo não é mais válido.)
-   Chama o método [**CBaseRenderer:: CompleteStateChange**](cbaserenderer-completestatechange.md) e retorna o valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




