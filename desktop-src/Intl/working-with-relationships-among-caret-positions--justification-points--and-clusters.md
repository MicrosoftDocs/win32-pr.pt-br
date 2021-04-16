---
description: A tabela a seguir mostra os vários métodos que o aplicativo pode usar para lidar com o cursor, a justificativa e os clusters.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Trabalhando com relações entre posições de cursor, pontos de justificações e clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757976"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Trabalhando com relações entre posições de cursor, pontos de justificações e clusters

A tabela a seguir mostra os vários métodos que o aplicativo pode usar para lidar com o cursor, a justificativa e os clusters.



| Tarefa                             | Suporte ao Uniscribe                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Movimento do cursor por cluster de caracteres  | O parâmetro *pwLogClust* do [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** membro da estrutura de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> O membro **fCharStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Quebra de linha entre caracteres | O parâmetro *pwLogClust* do [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** membro da estrutura de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> O membro **fCharStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Mover o cursor por palavra               | O membro **fWordStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Quebra de linha entre palavras      | O membro **fWordStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Justificativa                    | O membro **uJustification** da estrutura [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr)                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




