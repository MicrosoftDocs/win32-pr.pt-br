---
description: Passa uma mensagem de alteração de tamanho de vídeo do EC \_ \_ \_ para o Gerenciador do grafo de filtro.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Método CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
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
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780892"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>Método CBaseControlVideo. OnVideoSizeChange

Passa uma mensagem de alteração de tamanho de vídeo do EC \_ \_ \_ para o Gerenciador do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                   | Descrição               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>        | Falha.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/> |



 

## <a name="remarks"></a>Comentários

Um processador de vídeo deve chamar essa função de membro toda vez que o tamanho do vídeo for alterado; Isso normalmente será chamado uma vez após a conexão inicial. Se o renderizador puder dar suporte a alterações de formato dinâmico (de 320 x 240 a 160 x 120), ele também deverá chamá-la após cada alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




