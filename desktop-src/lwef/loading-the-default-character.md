---
title: Carregando o caractere padrão
description: Carregando o caractere padrão
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105786133"
---
# <a name="loading-the-default-character"></a>Carregando o caractere padrão

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Em vez de carregar apenas um caractere específico diretamente especificando seu nome de arquivo, você pode carregar o *caractere padrão*. O caractere padrão é um serviço destinado a fornecer um assistente do Windows central e compartilhado que o usuário escolhe. O Microsoft Agent inclui uma folha de propriedades como parte do serviço de caractere padrão, conhecido como o caractere janela Propriedades, que permite que o usuário altere a seleção do caractere padrão.

A seleção do caractere padrão é limitada a um caractere que dá suporte ao conjunto de animações padrão, garantindo um nível básico de consistência entre os caracteres. Isso não exclui um caractere de ter animações adicionais.

No entanto, como o caractere padrão destina-se ao uso para fins gerais e pode ser compartilhado por outros aplicativos ao mesmo tempo, evite carregar o caractere padrão quando desejar um caractere exclusivamente para seu aplicativo.

Para carregar o caractere padrão, chame o método [**Load**](load-method.md) sem especificar um nome de arquivo ou caminho. O Microsoft Agent carrega automaticamente o conjunto de caracteres atual como o caractere padrão. Se o usuário ainda não tiver selecionado um caractere padrão, o Agent selecionará o primeiro caractere que dá suporte ao conjunto de animações padrão. Se nenhum estiver disponível, o método falhará e relatará a causa.

Embora um aplicativo cliente possa consultar a identidade do caractere, apenas um usuário pode alterar suas configurações. Você pode usar o [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) para exibir o caractere janela Propriedades.

O servidor notificará os clientes que carregaram o caractere padrão quando um usuário alterar uma seleção de caracteres e passar o GUID do novo caractere. O servidor descarrega automaticamente o caractere anterior e recarrega o novo caractere. As filas de todos os clientes que carregaram o caractere padrão são interrompidas e liberadas. No entanto, as filas de clientes que carregaram o caractere explicitamente usando o nome de arquivo do caractere não são afetadas. Se necessário, o servidor também lida automaticamente com a redefinição automática do mecanismo de conversão de texto em fala (TTS) para o novo caractere.

 

 




