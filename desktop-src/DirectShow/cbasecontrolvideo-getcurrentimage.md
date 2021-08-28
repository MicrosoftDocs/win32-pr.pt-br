---
description: O método GetCurrentImage recupera uma cópia da imagem atual no renderador.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Método CBaseControlVideo.GetCurrentImage (Ctlutil.h)
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
ms.openlocfilehash: 782f540959b134f7ca00c2bc674a64ce60ccb4f6ddf166c79f2597e582ca9fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087566"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>Método CBaseControlVideo.GetCurrentImage

O `GetCurrentImage` método recupera uma cópia da imagem atual no renderador.

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

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                        | Descrição                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>             | Falha.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argumento inválido.<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Sem memória. Retornado quando o *parâmetro pVideoInfo* é **NULL.**<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Êxito.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ NÃO \_ PAUSADO**</dt> </dl> | Não foi possível realizar a operação porque o filtro não está em pausa.<br/> |



 

## <a name="remarks"></a>Comentários

Essa função membro recupera a imagem do exemplo e a copia para o buffer de saída. A seção do vídeo copiado para o buffer de saída reflete o retângulo de origem definido por meio da interface [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Ele não reflete o retângulo de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




