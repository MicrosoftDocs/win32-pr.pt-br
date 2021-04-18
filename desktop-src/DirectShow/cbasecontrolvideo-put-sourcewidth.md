---
description: O \_ método Put SourceWidth define a largura do retângulo de origem.
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: Método de CBaseControlVideo.put_SourceWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1576389a90db71ee6d371f6e68c44ea39117c05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756829"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a>Método CBaseControlVideo. put \_ SourceWidth

O `put_SourceWidth` método define a largura do retângulo de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SourceWidth* 
</dt> <dd>

Nova largura do retângulo de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argumento inválido.<br/>                                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | A operação não pode ser executada porque os Pins não estão conectados.<br/> |



 

## <a name="remarks"></a>Comentários

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

 

 




