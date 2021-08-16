---
title: Efeito pré-multiply
description: Use esse efeito para converter uma imagem de alfa não pré-convertido em alfa pré-convertido.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- efeito premultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af158ab8f885c51d2dce15d5bfbc5c24f34f6a980ebc8e8f4631617d31a2a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075020"
---
# <a name="premultiply-effect"></a>Efeito pré-multiply

Use esse efeito para converter uma imagem de alfa não pré-convertido em alfa pré-convertido. O efeito substitui cada pixel de `P = {R, G, B, A}` entrada `P' = {R*A, G*A, B*A, A}` por na saída.

Esse efeito não tem propriedades.

O CLSID para esse efeito é CLSID \_ D2D1Premultiply.

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
