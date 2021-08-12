---
title: Efeito de metadados de opacidade
description: Você pode usar esse efeito para marcar uma área de uma imagem de entrada como opaca, de modo que as otimizações de renderização internas para o grafo sejam possíveis.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be14699214337dc3f8c6e9e525f128a382c14ee479af08b99ea1f9eadd00041d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665316"
---
# <a name="opacity-metadata-effect"></a>Efeito de metadados de opacidade

Você pode usar esse efeito para marcar uma área de uma imagem de entrada como opaca, de modo que as otimizações de renderização internas para o grafo sejam possíveis.

> [!Note]  
> Esse efeito não modifica a imagem em si para ser opaca. Ele modifica os dados associados à imagem para que o renderista assuma que a região especificada é opaca.

 

O CLSID para esse efeito é CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                 | Tipo e valor padrão                                                             | Descrição                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ PROP \_ INPUT \_ OPAQUE \_ RECT <br/> | D2D1 \_ VECTOR \_ 4F<br/> (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX) <br/> | A parte da imagem de origem que é opaca. O padrão é toda a imagem de entrada.<br/> |



 

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

 

