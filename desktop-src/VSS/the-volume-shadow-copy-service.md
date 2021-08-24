---
description: o Serviço de Cópias de Sombra de Volume (VSS) fornece a infraestrutura do sistema para executar aplicativos VSS em sistemas baseados em Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: O Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71e21ba0f20eaa0f3723cd0da6cb3efb89bae027678d154ab8b5b5568532ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866236"
---
# <a name="the-volume-shadow-copy-service"></a>O Serviço de Cópias de Sombra de Volume

o Serviço de Cópias de Sombra de Volume (VSS) fornece a infraestrutura do sistema para executar aplicativos VSS em sistemas baseados em Windows.

Embora seja amplamente transparente para o usuário e o desenvolvedor, o VSS faz o seguinte:

-   Coordena atividades de provedores, gravadores e solicitantes na criação e no uso de cópias de sombra
-   Fornece o provedor de sistema padrão
-   Implementa a funcionalidade de driver de nível baixo necessária para que qualquer provedor funcione

O serviço VSS é iniciado sob demanda; portanto, para que as operações do VSS sejam bem-sucedidas, esse serviço precisa ser habilitado.

 

 



