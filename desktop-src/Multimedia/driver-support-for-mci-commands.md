---
title: Suporte de driver para comandos MCI
description: Suporte de driver para comandos MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2aa2bb806e869adcf4355b8b43ac529240a5c35dfc8ce49d43672baf0bd976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526286"
---
# <a name="driver-support-for-mci-commands"></a>Suporte de driver para comandos MCI

Os drivers MCI fornecem a funcionalidade para comandos MCI. O software do sistema executa algumas tarefas básicas de gerenciamento de dados, mas toda a reprodução, apresentação e gravação multimídia é manipulada pelos drivers MCI individuais.

Os drivers variam em seu suporte para comandos MCI e sinalizadores de comando. Como os dispositivos multimídia podem ter funcionalidades amplamente diferentes, a MCI foi projetada para permitir que drivers individuais estendam ou reduzam os conjuntos de comandos para corresponder aos recursos do dispositivo. Por exemplo, o comando [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) faz parte do conjunto de comandos para sequenciadores MIDI, mas o driver MCISEQ incluído no Windows não dá suporte a esse comando. O tópico de referência para o comando record explica que os dispositivos do tipo de dispositivo **sequencer** reconhecem o comando ; Isso não significa que todos os dispositivos desse tipo são compatíveis com o comando . Os aplicativos devem [**usar o comando**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar os recursos de um dispositivo específico.

 

 




