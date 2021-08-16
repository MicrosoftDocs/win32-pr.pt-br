---
title: Atualizando da versão anterior
description: Atualizando da versão anterior
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de894f220db7ee09847a8fa767e1f99c38cee8014cb86b65c1251e0579eaabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745719"
---
# <a name="updating-from-previous-version"></a>Atualizando da versão anterior

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os aplicativos compilados com a versão 1.5 anterior do Microsoft Agent devem ser executados sem modificação na nova versão 2.0. A [**propriedade Connected**](connected-property.md) não pode mais ser definida como **False**; determinadas propriedades do objeto SpeechInput que foram substituídas ainda existem, mas não transformam mais nenhum valor, e o servidor não dispara mais os eventos [**de**](https://www.bing.com/search?q=**Restart**) Reinicialização [**e**](https://www.bing.com/search?q=**Shutdown**) Desligamento.

No entanto, se você atualizar seus aplicativos para usar o controle Agent 2.0, talvez seja preciso modificar seu código. Se você tiver instalado a versão 2.0 do Microsoft Agent e carregar um projeto do Visual Basic usar a versão anterior do controle Agent, o Visual Basic incluirá uma opção que exibirá automaticamente uma mensagem indicando que ele detectou uma nova versão do controle. Para garantir a operação adequada do seu aplicativo, sempre opte por usar a versão posterior.

Para outras linguagens de programação (como Microsoft Office 97 VBA), para atualizar o controle, talvez seja preciso primeiro remover o controle agente 1.5 e salvar o código. Em seguida, saia do ambiente de programação, reinicie o ambiente de programação, recarregue o código e insira o novo controle. Evite editar um aplicativo habilitado para o Agent 2.0 na mesma instância do ambiente de programação em que você está editando um aplicativo habilitado para Agent 1.5. Alguns ambientes de programação podem não lidar com as diferenças entre as duas versões de controles.

Você deve ser capaz de desinstalar a versão do Agent 1.5 em seu sistema depois de instalar a versão do Agent 2.0. No entanto, se o Agent 1.5 estiver instalado na versão 2.0, talvez seja preciso reinstalar o 2.0.

 

 




