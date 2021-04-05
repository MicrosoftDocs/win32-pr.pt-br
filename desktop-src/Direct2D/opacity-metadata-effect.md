---
title: Efeito de metadados de opacidade
description: Você pode usar esse efeito para marcar uma área de uma imagem de entrada como opaca, para que as otimizações de renderização internas para o grafo sejam possíveis.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086145"
---
# <a name="opacity-metadata-effect"></a>Efeito de metadados de opacidade

Você pode usar esse efeito para marcar uma área de uma imagem de entrada como opaca, para que as otimizações de renderização internas para o grafo sejam possíveis.

> [!Note]  
> Esse efeito não modifica a imagem em si para ser opaco. Ele modifica os dados associados à imagem para que o renderizador assuma que a região especificada é opaca.

 

O CLSID para esse efeito é CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                 | Tipo e valor padrão                                                             | Descrição                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ propu \_ entrada \_ opaca com \_ Rect <br/> | \_4F de vetor d2d1 \_<br/> (-FLT \_ MAX,-FLT \_ Max, FLT \_ Max, FLT \_ Max) <br/> | A parte da imagem de origem opaca. O padrão é a imagem de entrada inteira.<br/> |



 

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

 

