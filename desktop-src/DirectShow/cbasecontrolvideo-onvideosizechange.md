---
description: Passa uma mensagem EC \_ VIDEO SIZE CHANGED para o gerenciador de \_ \_ grafo de filtro.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Método CBaseControlVideo.OnVideoSizeChange (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 689f6f14426d88270136d6cc3687f9e214b72d6e42e2af44f3d189510d61f327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076686"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>Método CBaseControlVideo.OnVideoSizeChange

Passa uma mensagem EC \_ VIDEO SIZE CHANGED para o gerenciador de \_ \_ grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                   | Descrição               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Falha.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/> |



 

## <a name="remarks"></a>Comentários

Um renderador de vídeo deve chamar essa função de membro sempre que o tamanho do vídeo for alterado; isso normalmente será chamado uma vez após a conexão inicial. Se o renderador puder dar suporte a alterações de formato dinâmico (de 320 x 240 para 160 x 120), ele também deverá chamá-lo após cada alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




