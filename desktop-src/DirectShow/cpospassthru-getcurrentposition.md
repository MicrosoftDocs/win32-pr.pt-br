---
description: 'O método GetCurrentPosition recupera a posição atual, em relação à duração total do fluxo. Esse método implementa o método IMediaSeeking:: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Método CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a43477d019639b4e1de5c2aa40f18c99f7b902498c671f8106d5832c43b11584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084156"
---
# <a name="cpospassthrugetcurrentposition-method"></a>Método CPosPassThru. GetCurrentPosition

O `GetCurrentPosition` método recupera a posição atual, em relação à duração total do fluxo. Esse método implementa o método [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição atual, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Não há suporte para o método.<br/>   |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) para recuperar a posição mais recente. Se **GetMediaTime** falhar, o método chamará **IMediaSeeking:: getCurrentPosition** no PIN conectado.

O método **GetMediaTime** falha, por padrão, na classe base. Se o filtro armazenar a posição atual em cache, substitua **GetMediaTime** para retornar o valor armazenado em cache.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




