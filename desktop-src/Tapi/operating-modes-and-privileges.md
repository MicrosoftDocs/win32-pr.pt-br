---
description: O aplicativo pode solicitar um dos dois modos de operação ao abrir um dispositivo de telefone.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modos de operação e privilégios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f7d3c1f6b7049c3986b96734a537906dc62166c48d62e549684cdaa6d35ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012466"
---
# <a name="operating-modes-and-privileges"></a>Modos de operação e privilégios

O aplicativo pode solicitar um dos dois modos de operação ao abrir um dispositivo de telefone. Esses modos refletem os privilégios que o aplicativo solicita para o dispositivo:

-   Abrir um telefone para monitorar privilégios permite que o aplicativo determine o status do dispositivo de telefone. As mensagens são enviadas ao aplicativo quando o status é alterado no dispositivo de telefone é detectado.
-   Um aplicativo que abre um dispositivo de telefone para privilégios de proprietário pode usar operações que modificam o estado do dispositivo de telefone. O privilégio de proprietário também inclui automaticamente privilégios de monitor completo. A qualquer momento, um determinado dispositivo de telefone pode ser aberto apenas uma vez para privilégios de proprietário, mas várias vezes para os privilégios de monitor. Todas as operações de **phoneset** exigem privilégios de proprietário, enquanto todas as operações de **phoneGet** exigem apenas o monitoramento de privilégios.

 

 



