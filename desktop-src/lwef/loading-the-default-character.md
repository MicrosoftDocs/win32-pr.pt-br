---
title: Carregando o caractere padrão
description: Carregando o caractere padrão
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f99d194843c6196f69e287857ce08097e849f328738c5f5d1a6e7feba0c53d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247603"
---
# <a name="loading-the-default-character"></a>Carregando o caractere padrão

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Em vez de carregar apenas um caractere específico diretamente especificando seu nome de arquivo, você pode carregar o *caractere padrão*. O caractere padrão é um serviço destinado a fornecer um assistente de Windows compartilhado que o usuário escolher. O Microsoft Agent inclui uma folha de propriedades como parte do serviço de caractere padrão, conhecido como Caractere janela Propriedades, que permite que o usuário altere sua seleção do caractere padrão.

A seleção do caractere padrão é limitada a um caractere que dá suporte ao conjunto de animação padrão, garantindo um nível básico de consistência entre caracteres. Isso não exclui um caractere de ter animações adicionais.

No entanto, como o caractere padrão destina-se ao uso de uso geral e pode ser compartilhado por outros aplicativos ao mesmo tempo, evite carregar o caractere padrão quando você quiser um caractere exclusivamente para seu aplicativo.

Para carregar o caractere padrão, chame o [**método Load**](load-method.md) sem especificar um nome de arquivo ou caminho. O Microsoft Agent carrega automaticamente o conjunto de caracteres atual como o caractere padrão. Se o usuário ainda não tiver selecionado um caractere padrão, o Agent selecionará o primeiro caractere que dá suporte ao conjunto de animação padrão. Se nenhum estiver disponível, o método falhará e relatará a causa.

Embora um aplicativo cliente possa perguntar sobre a identidade do caractere, somente um usuário pode alterar suas configurações. Você pode usar [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) para exibir o caractere janela Propriedades.

O servidor notificará os clientes que carregaram o caractere padrão quando um usuário altera uma seleção de caracteres e passará o GUID do novo caractere. O servidor descarrega automaticamente o caractere antigo e recarrega o novo caractere. As filas de todos os clientes que carregaram o caractere padrão são interrompidas e liberados. No entanto, as filas de clientes que carregaram o caractere explicitamente usando o nome de arquivo do caractere não são afetadas. Se necessário, o servidor também lida com a redefinição automática do mecanismo de TTS (texto em fala) para o novo caractere.

 

 




