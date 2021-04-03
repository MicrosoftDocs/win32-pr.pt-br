---
title: Método Unadvise IReferenceClock
description: O método Unadvise cancela uma solicitação de notificação.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Método Unadvise Windows Media Format
- Método Unadvise Windows Media Format, interface IReferenceClock
- Formato de mídia do Windows da interface IReferenceClock, método Unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084226"
---
# <a name="ireferenceclockunadvise-method"></a>Método IReferenceClock:: Unadvise

O método **Unadvise** cancela uma solicitação de notificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificador da solicitação a ser removida. Use o valor retornado por AdviseTime no parâmetro pdwAdviseCookie.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                             | Descrição                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O método foi bem-sucedido.<br/>                    |
| <dl> <dt>**\_falso**</dt> </dl> | O identificador passado não existe.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





