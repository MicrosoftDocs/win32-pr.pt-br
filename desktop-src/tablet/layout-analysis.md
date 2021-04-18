---
description: A análise de layout opera em uma coleção de traços e classifica os traços em elementos manuscritos e de desenho. O objeto divisória fornece acesso aos recursos de análise de layout do Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Análise de layout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793737"
---
# <a name="layout-analysis"></a>Análise de layout

A análise de layout opera em uma coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e classifica os traços em elementos manuscritos e de desenho. O objeto [**divisória**](inkdivider-class.md) fornece acesso aos recursos de análise de layout do Tablet PC.

A tabela a seguir descreve os tipos de elementos estruturais da enumeração [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) em que o objeto [**divisória**](inkdivider-class.md) classifica os traços.



| Tipo          | Descrição                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segment**   | Um segmento de reconhecimento.<br/>                                                |
| **Linha**      | Uma linha de manuscrito que contém um ou mais segmentos de reconhecimento.<br/> |
| **Paragraph** | Um bloco de traços que contém uma ou mais linhas de manuscrito.<br/>    |
| **Senha**   | Tinta que não é manuscrito.<br/>                                          |



 

O objeto [**divisória**](inkdivider-class.md) tem uma coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , que o objeto **divisória** analisa dinamicamente cada vez que você adiciona ou exclui da coleção. O objeto **divisória** não é serializável e você não pode salvar seu estado de análise. Portanto, o objeto **divisória** é projetado para aplicativos que devem diferenciar a entrada de desenho e de manuscrito misturada, mas não precisam reanalisar grandes quantidades de tinta entre sessões.

Você pode obter um instantâneo estático do resultado da análise atual, que é retornado em um objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) . Você pode obter objetos [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , cada um representando um único elemento estrutural de um objeto **DivisionResult** . Os objetos **DivisionResult** e **DivisionUnit** não são serializáveis. No entanto, as informações de estado desses objetos estão disponíveis.

O objeto [**divisória**](inkdivider-class.md) funciona apenas com manuscrito da esquerda para a direita. Para que o objeto **divisória** analise idiomas verticais, como chinês corretamente, os caracteres devem ser desenhados da esquerda para a direita em vez de cima para baixo.

 

