---
title: Opções de teste de clique
description: Esta seção lista os valores de opção que são usados com o parâmetro dwOptions da função HitTestThemeBackground. Para obter uma lista dos valores retornados quando você especifica uma dessas opções, consulte valores de retorno de teste de clique.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638a7aaca83c658ad852b195cdb9514210a14c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453609"
---
# <a name="hit-test-options"></a>Opções de teste de clique

Esta seção lista os valores de opção que são usados com o parâmetro *dwOptions* da função [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Para obter uma lista dos valores retornados quando você especifica uma dessas opções, consulte [valores de retorno de teste de clique](theme-hit-test-retval.md).

## <a name="option-values"></a>Valores de opção

A tabela a seguir lista as opções de teste de clique.



| Opção                       | Valor                                                                                                                    | Descrição                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | Opção de teste de colisão do segmento em segundo plano.                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | Opção de teste de colisão de borda fixa.                                                                                                                                                       |
| \_legenda HTTB                | 0x00000004                                                                                                               | Opção de teste de clique de legenda.                                                                                                                                                            |
| HTTB \_ RESIZINGBORDER         | (HTTB \_ RESIZINGBORDER \_ Left \| HTTB \_ RESIZINGBORDER \_ Top \| HTTB \_ RESIZINGBORDERly \_ \| HTTB \_ RESIZINGBORDER \_ Bottom) | Redimensionando opções de teste de colisão de borda.                                                                                                                                                   |
| HTTB \_ RESIZINGBORDER \_ Left   | 0x00000010                                                                                                               | Redimensionando a opção de teste de clique da borda esquerda.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ superior    | 0x00000020                                                                                                               | Redimensionando a opção de teste de colisão de borda superior.                                                                                                                                                |
| HTTB \_ RESIZINGBORDER \_ Right  | 0x00000040                                                                                                               | Redimensionando a opção de teste de colisão de borda direita.                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ inferior | 0x00000080                                                                                                               | Redimensionando a opção de teste de colisão de borda inferior.                                                                                                                                             |
| HTTB \_ SizingTemplate         | 0x00000100                                                                                                               | A borda de redimensionamento é especificada como um modelo, não apenas bordas da janela. Essa opção é mutuamente exclusiva com HTTB \_ SYSTEMSIZINGMARGINS; HTTB \_ SizingTemplate tem precedência.         |
| HTTB \_ SYSTEMSIZINGMARGINS    | 0x00000200                                                                                                               | Usa a largura da borda de redimensionamento do sistema em vez das margens de conteúdo do estilo visual. Essa opção é mutuamente exclusiva com HTTB \_ SizingTemplate; HTTB \_ SizingTemplate tem precedência. |



 

 

 




