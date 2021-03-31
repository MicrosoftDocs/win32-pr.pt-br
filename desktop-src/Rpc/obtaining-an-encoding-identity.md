---
title: Obtendo uma identidade de codificação
description: Um aplicativo que está decodificando dados codificados pode obter a identidade da rotina usada para codificar os dados, antes de chamar uma rotina para decodificá-lo. A rotina MesInqProcEncodingId fornece essa identidade.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Chamada de procedimento remoto RPC, tarefas, obtendo identidade de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636759"
---
# <a name="obtaining-an-encoding-identity"></a>Obtendo uma identidade de codificação

Um aplicativo que está decodificando dados codificados pode obter a identidade da rotina usada para codificar os dados, antes de chamar uma rotina para decodificá-lo. A rotina [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fornece essa identidade.

Cada procedimento em uma interface é atribuído a um número de identificação de número inteiro, chamado de *identificador de procedimento* ou *ID de proc*, pelo compilador MIDL. A numeração começa com zero. As bibliotecas de tempo de execução RPC não estão envolvidas na conversão da ID do procedimento em uma chamada de procedimento real. Dada uma ID proc, seu aplicativo deve fornecer um meio de chamar o procedimento correto. Normalmente, os desenvolvedores de aplicativos usam uma série de instruções **If** ou (ao usar C/C++) uma instrução **switch** para essa finalidade.

 

 




