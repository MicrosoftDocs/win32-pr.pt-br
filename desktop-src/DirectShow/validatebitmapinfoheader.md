---
description: A função ValidateBitmapInfoHeader verifica uma estrutura de BITMAPINFOHEADER para determinados erros comuns que podem causar estouros de buffer ou estouro de número inteiro.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Função ValidateBitmapInfoHeader (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759108"
---
# <a name="validatebitmapinfoheader-function"></a>Função ValidateBitmapInfoHeader

A `ValidateBitmapInfoHeader` função verifica uma estrutura de [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) para determinados erros comuns que podem causar estouros de buffer ou estouro de número inteiro.

> [!Note]  
> Essa função não garante que a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seja válida ou que o código que usa a estrutura seja seguro.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbmi* 
</dt> <dd>

Ponteiro para a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) a ser validada.

</dd> <dt>

*cbSize* 
</dt> <dd>

Tamanho do bloco de memória que contém a estrutura, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor booliano. Se o valor for **false**, a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) não será válida.

## <a name="remarks"></a>Comentários

Essa função protege os seguintes erros:

-   Estouro aritmético no tamanho da estrutura ou em um tamanho de estrutura inválido.
-   Valor inválido para o membro **biClrUsed** .
-   Estouro aritmético no tamanho da imagem (**biSizeImage**).
-   Valores inválidos para o tamanho da imagem (**biSizeImage**) para formatos RGB.

A função não verifica se a estrutura descreve um formato de vídeo válido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




