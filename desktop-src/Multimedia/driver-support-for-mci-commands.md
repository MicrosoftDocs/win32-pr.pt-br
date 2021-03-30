---
title: Suporte de driver para comandos MCI
description: Suporte de driver para comandos MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635597"
---
# <a name="driver-support-for-mci-commands"></a>Suporte de driver para comandos MCI

Os drivers MCI fornecem a funcionalidade para comandos MCI. O software do sistema executa algumas tarefas básicas de gerenciamento de dados, mas toda a reprodução, apresentação e gravação de multimídia é tratada pelos drivers MCI individuais.

Os drivers variam em seu suporte para comandos MCI e sinalizadores de comando. Como os dispositivos de multimídia podem ter recursos amplamente diferentes, o MCI foi projetado para permitir que drivers individuais estendam ou reduzam os conjuntos de comandos para corresponder aos recursos do dispositivo. Por exemplo, o comando [**Record**](record.md) ([**\_ registro MCI**](mci-record.md)) faz parte do conjunto de comandos para sequenciadores MIDI, mas o driver MCISEQ incluído com o Windows não oferece suporte a esse comando. O tópico de referência para o comando de registro explica que os dispositivos do tipo de dispositivo **Sequencer** reconhecem o comando; Isso não significa que todos os dispositivos desse tipo dão suporte ao comando. Os aplicativos devem usar o comando de [**capacidade**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar os recursos de um dispositivo específico.

 

 




