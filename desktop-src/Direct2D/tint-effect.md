---
title: Efeito de tonalidade
description: Esse efeito dicolori a imagem de origem multiplicando a imagem de origem pela cor especificada. Ele tem uma única entrada.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918378"
---
# <a name="tint-effect"></a>Efeito de tonalidade

Esse efeito dicolori a imagem de origem multiplicando a imagem de origem pela cor especificada. Ele tem uma única entrada.

O CLSID para esse efeito é CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                    | Tipo e valor padrão                              | Descrição                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| Cor de prop ColorD2D1 de \_ tonalidade \_ \_<br/>               | \_ \_ 4F de vetor d2d1 (1,0 f, 1,0 f, 1,0 f, 1,0 f)<br/> | As cores da imagem de origem são multiplicadas por esse valor.       |
| \_Saída de \_ \_ fixe \_ de diClampOutputD2D1 de tonalidade<br/> | BOOLFALSE<br/>                                | Se deseja ou não fixe os valores de saída para o intervalo de \[ 0, 1 \] . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |



 ## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
