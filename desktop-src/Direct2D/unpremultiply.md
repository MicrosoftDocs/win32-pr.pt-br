---
title: Efeito de Unpremultiply
description: Use esse efeito para converter uma imagem de alfa-geomultiplicado Alpha para unpremultiplied Alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- efeito de unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369817"
---
# <a name="unpremultiply-effect"></a>Efeito de Unpremultiply

Use esse efeito para converter uma imagem de alfa-geomultiplicado Alpha para unpremultiplied Alpha. O efeito substitui cada pixel de entrada `P = {R, G, B, A}` por `P' = {R/A, G/A, B/A, A}` na saída.

Esse efeito não tem propriedades.

O CLSID para esse efeito é CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
