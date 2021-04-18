---
description: O método GetCurrentImage recupera uma cópia da imagem atual no renderizador.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Método CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767686"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>Método CBaseControlVideo. GetCurrentImage

O `GetCurrentImage` método recupera uma cópia da imagem atual no renderizador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Ponteiro para o tamanho do buffer de saída.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Ponteiro para o buffer de saída da imagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                        | Descrição                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>             | Falha.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argumento inválido.<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Sem memória. Retornado quando o parâmetro *pVideoInfo* é **nulo**.<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Êxito.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ não em \_ pausa**</dt> </dl> | A operação não pôde ser executada porque o filtro não está em pausa.<br/> |



 

## <a name="remarks"></a>Comentários

Essa função de membro recupera a imagem do exemplo e a copia para o buffer de saída. A seção de vídeo copiada no buffer de saída reflete o retângulo de origem definido por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Ele não reflete o retângulo de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




