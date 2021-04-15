---
title: Atualizando da versão anterior
description: Atualizando da versão anterior
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761205"
---
# <a name="updating-from-previous-version"></a>Atualizando da versão anterior

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Aplicativos compilados e compilados com a versão 1,5 anterior do Microsoft Agent devem ser executados sem modificação na nova versão 2,0. A propriedade [**Connected**](connected-property.md) não pode mais ser definida como **false**; algumas propriedades do objeto SpeechInput que foram substituídas ainda existem, mas não transformam mais nenhum valor, e o servidor não dispara mais os eventos de [**reinicialização**](https://www.bing.com/search?q=**Restart**) e [**desligamento**](https://www.bing.com/search?q=**Shutdown**) .

No entanto, se você atualizar seus aplicativos para usar o controle do agente 2,0, talvez seja necessário modificar seu código. Se você tiver instalado a versão 2,0 do Microsoft Agent e carregar um projeto de Visual Basic usar a versão anterior do controle do agente, Visual Basic incluirá uma opção que exibirá automaticamente uma mensagem indicando que ela detectou uma nova versão do controle. Para garantir a operação adequada do seu aplicativo, sempre escolha usar a versão mais recente.

Para outras linguagens de programação (como 97 Microsoft Office VBA), para atualizar o controle, talvez você precise primeiro remover o controle do agente 1,5 e salvar seu código. Em seguida, saia do ambiente de programação, reinicie o ambiente de programação, recarregue o código e insira o novo controle. Evite editar um aplicativo habilitado para agente 2,0 na mesma instância do ambiente de programação em que você está editando um aplicativo habilitado para agente 1,5 no. Alguns ambientes de programação podem não lidar com as diferenças entre as duas versões de controles.

Você deve ser capaz de desinstalar a versão do agente 1,5 no sistema depois de instalar a versão 2,0 do agente. No entanto, se o Agent 1,5 estiver instalado na versão 2,0, talvez seja necessário reinstalar o 2,0.

 

 




