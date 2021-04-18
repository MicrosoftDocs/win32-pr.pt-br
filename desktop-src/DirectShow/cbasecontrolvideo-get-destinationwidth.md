---
description: O \_ método Get DestinationWidth recupera a largura do retângulo de destino atual.
ms.assetid: 7d466d61-1768-48b4-8460-b15d28a294f3
title: Método de CBaseControlVideo.get_DestinationWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95fc5ccdf0c2b0dd6d198686e12edb3185489b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755623"
---
# <a name="cbasecontrolvideoget_destinationwidth-method"></a>CBaseControlVideo. obter \_ método DestinationWidth

O `get_DestinationWidth` método recupera a largura do retângulo de destino atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DestinationWidth(
   long *pDestinationWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestinationWidth* 
</dt> <dd>

Ponteiro para a largura de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | A operação não pode ser executada porque os Pins não estão conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |



 

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IBasicVideo:: get \_ DestinationWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationwidth) .

Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido. O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada. O canto superior esquerdo da janela é coordenada (0, 0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




