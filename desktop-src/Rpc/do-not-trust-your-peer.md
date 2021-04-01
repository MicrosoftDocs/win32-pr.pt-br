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
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="3a0df-103">Não confie no seu par</span><span class="sxs-lookup"><span data-stu-id="3a0df-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="3a0df-104">"Não confie no seu par" é uma regra de segurança básica, mas geralmente é ignorada.</span><span class="sxs-lookup"><span data-stu-id="3a0df-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="3a0df-105">Não presuma que a outra parte em uma comunicação se comportará corretamente e não presuma que seu par passará os dados esperados.</span><span class="sxs-lookup"><span data-stu-id="3a0df-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="3a0df-106">MIDL e RPC executam algumas verificações em seu nome, mas nem todas as verificações.</span><span class="sxs-lookup"><span data-stu-id="3a0df-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="3a0df-107">Saiba qual aspecto dos parâmetros são verificados por MIDL ou RPC e quais aspectos você deve verificar por conta própria.</span><span class="sxs-lookup"><span data-stu-id="3a0df-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="3a0df-108">Por exemplo, para identificadores de contexto in/out, o RPC verifica se o identificador de contexto não é um valor não nulo inválido.</span><span class="sxs-lookup"><span data-stu-id="3a0df-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="3a0df-109">Ele permite valores nulos e valores válidos, mas muitos desenvolvedores não sabem que os valores nulos são possibilitados.</span><span class="sxs-lookup"><span data-stu-id="3a0df-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="3a0df-110">Isso é algo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="3a0df-110">This is something to check for.</span></span>

<span data-ttu-id="3a0df-111">Mesmo que você geralmente confie em seu par, não se esqueça de apresentar novos caminhos pelos quais uma máquina comprometida ou conta de entidade de segurança pode atacar outros computadores.</span><span class="sxs-lookup"><span data-stu-id="3a0df-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="3a0df-112">Imagine que um usuário escolha seu aniversário como sua senha e seja adivinhado por um invasor.</span><span class="sxs-lookup"><span data-stu-id="3a0df-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="3a0df-113">Mesmo depois que as solicitações do usuário são autenticadas e o acesso a seus dados é permitido, certifique-se de que as vulnerabilidades exploráveis não existam, tais saturações de pilha que podem permitir que um invasor assuma o controle do seu servidor e estenda a violação de segurança.</span><span class="sxs-lookup"><span data-stu-id="3a0df-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




