---
title: Efeito não impretipicamente
description: Use esse efeito para converter uma imagem de alfa pré-ultado em alfa não pré-convertido.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- efeito despremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152803956b9839b881404be013c521dc0f5bfc764b2f07a8462275b523ba762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664874"
---
# <a name="unpremultiply-effect"></a>Efeito não impretipicamente

Use esse efeito para converter uma imagem de alfa pré-ultado em alfa não pré-convertido. O efeito substitui cada pixel de `P = {R, G, B, A}` entrada `P' = {R/A, G/A, B/A, A}` por na saída.

Esse efeito não tem propriedades.

O CLSID para esse efeito é CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para aplicativos Windows 7 área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para aplicativos Windows 7 área de trabalho \[ \| Windows Store\] |
| parâmetro                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
