---
title: Não confie no seu par
description: '\ 0034; não confie no seu par \ 0034; é uma regra de segurança básica, mas geralmente é ignorada.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635723"
---
# <a name="do-not-trust-your-peer"></a>Não confie no seu par

"Não confie no seu par" é uma regra de segurança básica, mas geralmente é ignorada. Não presuma que a outra parte em uma comunicação se comportará corretamente e não presuma que seu par passará os dados esperados. MIDL e RPC executam algumas verificações em seu nome, mas nem todas as verificações.

Saiba qual aspecto dos parâmetros são verificados por MIDL ou RPC e quais aspectos você deve verificar por conta própria. Por exemplo, para identificadores de contexto in/out, o RPC verifica se o identificador de contexto não é um valor não nulo inválido. Ele permite valores nulos e valores válidos, mas muitos desenvolvedores não sabem que os valores nulos são possibilitados. Isso é algo a ser verificado.

Mesmo que você geralmente confie em seu par, não se esqueça de apresentar novos caminhos pelos quais uma máquina comprometida ou conta de entidade de segurança pode atacar outros computadores. Imagine que um usuário escolha seu aniversário como sua senha e seja adivinhado por um invasor. Mesmo depois que as solicitações do usuário são autenticadas e o acesso a seus dados é permitido, certifique-se de que as vulnerabilidades exploráveis não existam, tais saturações de pilha que podem permitir que um invasor assuma o controle do seu servidor e estenda a violação de segurança.

 

 




