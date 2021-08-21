---
description: O método GetStdDev estima o desvio padrão em milissegundos entre quando cada quadro é devido e quando ele é realmente renderizado, para estatísticas por quadro.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Método CBaseVideoRenderer.GetStdDev (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f7b6ab85000f537179fcc9ae6b979194ae4e975ea2b394d0c58afb8515158aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157078"
---
# <a name="cbasevideorenderergetstddev-method"></a>Método CBaseVideoRenderer.GetStdDev

O método estima o desvio padrão em milissegundos entre quando cada quadro é devido e quando ele é realmente renderizado, para estatísticas `GetStdDev` por quadro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nSamples* 
</dt> <dd>

Valor inteiro que contém o número de exemplos de vídeo recebidos pelo renderador de vídeo.

</dd> <dt>

*piResult* 
</dt> <dd>

Ponteiro para um valor inteiro que conterá o desvio padrão.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Valor que representa o desvio padrão, em milissegundos, de todos os exemplos de vídeo renderizados. Quanto menor o valor, mais consistente será a renderização.

</dd> <dt>

*iTot* 
</dt> <dd>

Valor que representa o valor médio, em milissegundos, entre o tempo marcado e o tempo renderizado para todos os exemplos de vídeo renderizados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna NOERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




