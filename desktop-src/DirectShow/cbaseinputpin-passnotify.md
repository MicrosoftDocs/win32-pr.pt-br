---
description: O método PassNotify Passa uma mensagem de controle de qualidade para o objeto apropriado.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Método CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771871"
---
# <a name="cbaseinputpinpassnotify-method"></a>Método CBaseInputPin. PassNotify

O `PassNotify` método passa uma mensagem de controle de qualidade para o objeto apropriado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*perguntas* 
</dt> <dd>

Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ não \_ encontrado**</dt> </dl> | Não foi possível encontrar um objeto para aceitar a mensagem.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método se o filtro não manipular mensagens de controle de qualidade. Esse método passa a mensagem para um dos seguintes objetos, em ordem de preferência:

-   Um Gerenciador de controle de qualidade externo, se o método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) foi chamado.
-   O pino de saída upstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> <dt>

[Gerenciamento de controle de qualidade](quality-control-management.md)
</dt> </dl>

 

 




