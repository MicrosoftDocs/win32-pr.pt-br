---
title: Efeito de tonalidade
description: Esse efeito define a imagem de origem multiplicando a imagem de origem pela cor especificada. Ele tem uma única entrada.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61734e9e060da4609927c9db46eee50dab1bef1e6328f304fdfb2436529289cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384906"
---
# <a name="tint-effect"></a>Efeito de tonalidade

Esse efeito define a imagem de origem multiplicando a imagem de origem pela cor especificada. Ele tem uma única entrada.

O CLSID para esse efeito é CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                    | Tipo e valor padrão                              | Description                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| ColorD2D1 \_ TINT \_ PROP \_ COLOR<br/>               | D2D1 \_ VECTOR \_ 4F(1.0f, 1.0f, 1.0f, 1.0f)<br/> | As cores da imagem de origem são multiplicadas por esse valor.       |
| Saída DE FIX FIX DO PROP \_ DE TINTOutputD2D1 \_ \_ \_<br/> | BOOLFALSE<br/>                                | Se deve ou não fixar os valores de saída no intervalo \[ 0, 1 \] . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Servidor mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| parâmetro                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |



 ## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
