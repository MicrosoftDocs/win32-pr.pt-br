---
description: Um monitor é uma DLL (biblioteca de vínculo dinâmico) que examina as capturas em tempo real do tráfego de rede.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920997"
---
# <a name="monitors"></a>Monitores

Um monitor é uma DLL (biblioteca de vínculo dinâmico) que examina as capturas em tempo real do tráfego de rede. Ele procura condições predefinidas e gera eventos quando essas condições são detectadas. Por exemplo, um evento pode ser acionado quando uma interrupção de rede é tentada, quando uma estação de trabalho não autorizada está distribuindo endereços IP ou quando um roteador falha.

> [!Note]  
> Se você precisar executar análises detalhadas em dados de rede que exijam uma análise após a captura, você deverá usar aplicativos de [*especialista*](e.md) e [*analisador*](p.md) .

 

O [*serviço de controle de monitor*](m.md) (MCSVC) fornece a estrutura para gerenciar seus monitores. Ele fornece funções para carregar as DLLs de monitor e uma interface de comunicação para a ferramenta de controle de monitor para que você possa criar, configurar, iniciar, parar e desabilitar várias instâncias de seus monitores.

Os monitores são executados em dois threads de execução. O MCSVC fornece o primeiro thread, que fornece controle direto do monitor. O segundo thread é fornecido pelo NPP ( [*provedor de pacotes de rede*](n.md) ), que fornece uma maneira de passar os dados de rede capturados, as estatísticas e o status da captura do NPP de volta para o monitor.

Mais de uma instância do mesmo monitor pode existir para cada interface NPP de tempo de execução usada para capturar dados.

 

 



