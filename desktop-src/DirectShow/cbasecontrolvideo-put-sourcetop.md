---
description: O método \_ put SourceTop define a coordenada superior do retângulo de origem.
ms.assetid: 8891771d-5a0b-4dfa-b961-9f375f13b4f7
title: CBaseControlVideo.put_SourceTop método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de7c0da0d38da2563e0a34b5f7f894a23e7b55390fc9291321dbca46a7cb61fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793846"
---
# <a name="cbasecontrolvideoput_sourcetop-method"></a>Método SourceTop CBaseControlVideo.put \_

O `put_SourceTop` método define a coordenada superior do retângulo de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_SourceTop(
   long SourceTop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SourceTop* 
</dt> <dd>

Nova coordenada superior do retângulo de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argumento inválido.<br/>                                                     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | Argumento de ponteiro **NULL.**<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | A operação não pode ser executada porque os pinos não estão conectados.<br/> |



 

## <a name="remarks"></a>Comentários

Um aplicativo pode alterar os retângulos de origem e de destino do vídeo por meio da interface [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for exibido. O retângulo de destino é relativo à área do cliente da janela na qual ele está sendo a reprodução. O canto superior esquerdo da janela é coordenado (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




