---
title: Resposta de leitor para recursos do ASF
description: Resposta de leitor para recursos do ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows SDK de Formato de Mídia, respostas de leitor para recursos do ASF
- ASF (Advanced Systems Format), respostas de leitor a recursos
- ASF (Formato de Sistemas Avançados), respostas de leitor a recursos
- respostas de leitor para recursos do ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8b8b64649388af6186155009f2a47b0f2b2c96cc42645e64dbb04f3054d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084493"
---
# <a name="reader-response-to-asf-features"></a>Resposta de leitor para recursos do ASF

A maioria dos recursos especiais de arquivo ASF pode ser definida em arquivos para interagir com aplicativos de reprodução personalizados projetados para lidar com eles. No entanto, alguns dos recursos têm suporte integrado no objeto de leitor.

O objeto leitor selecionará automaticamente fluxos de conjuntos que são mutuamente exclusivos por taxa de bits. Esse caso especial é conhecido como MBR (taxa de bits múltipla). O fluxo selecionado pelo leitor baseia-se na taxa de bits do fluxo. O número de fluxo e a ordem na qual ele foi adicionado ao objeto de exclusão mútua são irrelevantes para a seleção automática. Se um arquivo incluir mais de um conjunto de fluxos mutuamente exclusivos por taxa de bits, o leitor selecionará fluxos com base no cálculo do melhor uso da largura de banda disponível.

A exclusão mútua baseada em idioma é definida usando uma configuração de saída, antes da reprodução. Se você combinar a exclusão mútua baseada em taxa de bits e idioma, deverá agrupar os fluxos mutuamente exclusivos baseados em taxa de bits por idioma e, em seguida, tornar os grupos mutuamente exclusivos por idioma. O leitor verificará o idioma primeiro e, em seguida, determinará qual taxa de bits usar.

A priorização de fluxo é definida usando uma matriz de registros. Os registros na matriz estão em ordem decrescente de prioridade. O último fluxo na matriz é o primeiro que será descartado pelo leitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Exclusão mútua**](mutual-exclusion.md)
</dt> <dt>

[**Priorização de fluxo**](stream-prioritization.md)
</dt> </dl>

 

 




