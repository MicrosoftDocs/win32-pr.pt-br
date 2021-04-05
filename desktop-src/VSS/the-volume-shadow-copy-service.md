---
description: O Serviço de Cópias de Sombra de Volume (VSS) fornece a infraestrutura do sistema para executar aplicativos VSS em sistemas baseados no Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: O Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647175"
---
# <a name="the-volume-shadow-copy-service"></a>O Serviço de Cópias de Sombra de Volume

O Serviço de Cópias de Sombra de Volume (VSS) fornece a infraestrutura do sistema para executar aplicativos VSS em sistemas baseados no Windows.

Embora seja amplamente transparente para o usuário e o desenvolvedor, o VSS faz o seguinte:

-   Coordena atividades de provedores, gravadores e solicitantes na criação e no uso de cópias de sombra
-   Fornece o provedor de sistema padrão
-   Implementa a funcionalidade de driver de nível baixo necessária para que qualquer provedor funcione

O serviço VSS é iniciado sob demanda; portanto, para que as operações do VSS sejam bem-sucedidas, esse serviço precisa ser habilitado.

 

 



