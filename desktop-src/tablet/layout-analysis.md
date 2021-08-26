---
description: A análise de layout opera em uma coleção Strokes e classifica os traços em elementos de manuscrito e desenho. O objeto Divisor fornece acesso aos recursos de análise de layout do tablet pc.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Análise de layout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8131859dd7e4c7bd6927db42bd605541001ac0f1222bfbf27b0e59809d4b7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934816"
---
# <a name="layout-analysis"></a>Análise de layout

A análise de layout opera em uma coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e classifica os traços em elementos de manuscrito e desenho. O [**objeto Divisor**](inkdivider-class.md) fornece acesso aos recursos de análise de layout do tablet pc.

A tabela a seguir descreve os tipos de elementos estruturais da [**enumeração InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) na qual o objeto [**Divider**](inkdivider-class.md) classifica traços.



| Tipo          | Descrição                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segment**   | Um segmento de reconhecimento.<br/>                                                |
| **Linha**      | Uma linha de manuscrito que contém um ou mais segmentos de reconhecimento.<br/> |
| **Paragraph** | Um bloco de traços que contém uma ou mais linhas de manuscrito.<br/>    |
| **Desenho**   | Tinta que não é manuscrito.<br/>                                          |



 

O [**objeto Divider**](inkdivider-class.md) tem uma coleção [**Strokes,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o objeto **Divisor** analisa dinamicamente cada vez que você adiciona ou exclui da coleção. O **objeto Divider** não é serializável e você não pode salvar seu estado de análise. Portanto, **o objeto Divisor** foi projetado para aplicativos que devem diferenciar entre manuscrito misto e entrada de desenho, mas não precisam reanalizar grandes quantidades de tinta entre sessões.

Você pode obter um instantâneo estático do resultado da análise atual, que é retornado em um [**objeto DivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) Você pode obter [**objetos DivisionUnit,**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) cada um representando um único elemento estrutural de **um objeto DivisionResult.** Os **objetos DivisionResult** e **DivisionUnit** não são serializáveis. No entanto, as informações de estado desses objetos estão disponíveis.

O [**objeto Divisor**](inkdivider-class.md) funciona apenas com manuscrito da esquerda para a direita. Para que **o objeto Divisor** analise corretamente idiomas verticais, como chinês, os caracteres devem ser desenhados da esquerda para a direita, em vez de de cima para baixo.

 

