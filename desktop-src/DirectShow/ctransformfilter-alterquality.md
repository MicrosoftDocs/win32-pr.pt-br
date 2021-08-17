---
description: O método AlterQuality notifica o filtro de que uma alteração de qualidade é solicitada.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Método CTransformFilter.AlterQuality (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b9b136217c23f64bcd779f5c96189ca993646ffb29ce5316cf5913de8c9abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317146"
---
# <a name="ctransformfilteralterquality-method"></a>Método CTransformFilter.AlterQuality

O `AlterQuality` método notifica o filtro de que uma alteração de qualidade é solicitada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Q* 
</dt> <dd>

[**Estrutura**](/windows/win32/api/strmif/ns-strmif-quality) de qualidade que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                             | Description                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Não lidava com a mensagem de qualidade. A mensagem deve ser passada upstream.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Tratada a mensagem de qualidade. Nenhuma ação posterior é necessária.<br/>               |



 

## <a name="remarks"></a>Comentários

Substitua esse método se o filtro puder executar o controle de qualidade. Para obter mais informações, consulte [Gerenciamento de controle de qualidade.](quality-control-management.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




