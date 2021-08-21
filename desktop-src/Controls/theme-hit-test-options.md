---
title: Opções de teste de clique
description: Esta seção lista os valores de opção que são usados com o parâmetro dwOptions da função HitTestThemeBackground. Para obter uma lista dos valores retornados quando você especifica uma dessas opções, consulte valores de retorno de teste de clique.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e3f9f3c7ba8b5c7a2c4468177befc3083bb2ed613b674cdb02f7fd3ad7f10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166521"
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



 

 

 




