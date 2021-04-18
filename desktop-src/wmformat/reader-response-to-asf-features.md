---
title: Resposta do leitor para recursos do ASF
description: Resposta do leitor para recursos do ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- SDK do Windows Media Format, respostas do leitor para recursos do ASF
- ASF (Advanced Systems Format), respostas de leitor para recursos
- ASF (formato de sistemas avançados), respostas de leitor para recursos
- respostas do leitor para recursos do ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814086"
---
# <a name="reader-response-to-asf-features"></a>Resposta do leitor para recursos do ASF

A maioria dos recursos de arquivo ASF especiais pode ser definida em arquivos para interagir com aplicativos de reprodução personalizados projetados para tratá-los. No entanto, alguns dos recursos têm suporte interno no objeto leitor.

O objeto leitor selecionará automaticamente fluxos de conjuntos que são mutuamente exclusivos por taxa de bits. Esse caso especial é chamado de taxa de bits múltipla (MBR). O fluxo que o leitor seleciona é baseado na taxa de bits do fluxo. O número do fluxo e a ordem em que ele foi adicionado ao objeto de exclusão mútua são irrelevantes para a seleção automática. Se um arquivo incluir mais de um conjunto de fluxos mutuamente exclusivos por taxa de bits, o leitor selecionará fluxos com base no cálculo do melhor uso da largura de banda disponível.

A exclusão mútua baseada em linguagem é definida usando uma configuração de saída, antes da reprodução. Se você combinar o idioma e a exclusão mútua baseada em taxa de bits, deverá agrupar os fluxos mutuamente exclusivos baseados em taxa de bits por idioma e, em seguida, tornar os grupos mutuamente exclusivos por idioma. O leitor verificará o idioma primeiro e, em seguida, determinará qual taxa de bits usar.

A priorização de fluxo é definida usando uma matriz de registros. Os registros na matriz estão em ordem decrescente de prioridade. O último fluxo na matriz é o primeiro que será Descartado pelo leitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Exclusão mútua**](mutual-exclusion.md)
</dt> <dt>

[**Priorização de fluxo**](stream-prioritization.md)
</dt> </dl>

 

 




