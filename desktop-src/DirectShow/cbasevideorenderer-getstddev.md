---
description: O método GetStdDev estima o desvio padrão em milissegundos entre quando cada quadro é devido e quando é realmente renderizado para estatísticas por quadro.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Método CBaseVideoRenderer. GetStdDev (Renbase. h)
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
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755603"
---
# <a name="cbasevideorenderergetstddev-method"></a>Método CBaseVideoRenderer. GetStdDev

O `GetStdDev` método estima o desvio padrão em milissegundos entre quando cada quadro é devido e quando é realmente renderizado para estatísticas por quadro.

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

Valor inteiro que contém o número de amostras de vídeo recebidas pelo processador de vídeo.

</dd> <dt>

*piResult* 
</dt> <dd>

Ponteiro para um valor inteiro que conterá o desvio padrão.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Valor que representa o desvio padrão, em milissegundos, de todos os exemplos de vídeo renderizados. Quanto menor o valor, mais consistente é a renderização.

</dd> <dt>

*iTot* 
</dt> <dd>

Valor que representa o valor médio, em milissegundos, entre a hora carimbada e o tempo processado para todos os exemplos de vídeo renderizados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna NOERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




