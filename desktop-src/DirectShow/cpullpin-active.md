---
description: O método Ativo cria um thread de trabalho que recebe dados do pino de saída. Esse método também confirma o alocador.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Método CPullPin.Active (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6572ad0b415f4c1a51133d080e84a2e869787dea0c23614478b09c7b86296b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073520"
---
# <a name="cpullpinactive-method"></a>Método CPullPin.Active

O **método Ativo** cria um thread de trabalho que recebe dados do pino de saída. Esse método também confirma o alocador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | A conexão de pino não foi estabelecida corretamente.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Não foi possível criar o thread ou o thread já existe.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método quando o filtro de propriedade ficar ativo. (Se o pin de entrada derivar [**de CBasePin,**](cbasepin.md)substitua o [**método CBasePin::Active.)**](cbasepin-active.md)

Antes de chamar esse método, chame o [**método CPullPin::Conexão**](cpullpin-connect.md) para estabelecer a conexão com o pino de saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




