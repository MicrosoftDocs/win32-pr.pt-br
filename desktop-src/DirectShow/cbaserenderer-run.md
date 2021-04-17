---
description: O método Run executa o filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Método CBaseRenderer. Run (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754994"
---
# <a name="cbaserendererrun-method"></a>Método CBaseRenderer. Run

O `Run` método executa o filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseFilter:: Run**](cbasefilter-run.md) . Ele executa as seguintes ações:

-   Chama o método **CBaseFilter:: Run** .
-   Confirma o alocador. (Consulte [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Se o estado anterior foi interrompido, o filtro libera qualquer amostra que está segurando. (O exemplo não é mais válido.)
-   Chama o método [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) e retorna o resultado. Se um exemplo estiver pendente, o método **StartStreaming** o agendará para renderização.

Se o filtro não estiver conectado, ele lançará um evento de [**\_ conclusão do EC**](ec-complete.md) imediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




