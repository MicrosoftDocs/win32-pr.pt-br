---
description: Componentes de ponto do Windows para pessoas ao meu redor
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Componentes de ponto do Windows para pessoas ao meu redor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921755"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="ed373-103">Componentes de ponto do Windows para pessoas ao meu redor</span><span class="sxs-lookup"><span data-stu-id="ed373-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="ed373-104">Dentro do executável principal da rede de pares do Windows (P2phost.exe), a [arquitetura pessoas ao meu redor](people-near-me-architecture.md) usa os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="ed373-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="ed373-105">Pessoas ao meu redor</span><span class="sxs-lookup"><span data-stu-id="ed373-105">People Near Me</span></span>

<span data-ttu-id="ed373-106">O componente pessoas ao meu redor (PNM) inicia a descoberta usando a descoberta de serviços da Web na sub-rede local para os nomes de usuário dos computadores compatíveis com o PNM.</span><span class="sxs-lookup"><span data-stu-id="ed373-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="ed373-107">Editor de pessoas ao meu redor</span><span class="sxs-lookup"><span data-stu-id="ed373-107">People Near Me Publisher</span></span>

<span data-ttu-id="ed373-108">O componente pessoas ao meu redor do editor publica os apelidos dos usuários conectados para indicar a disponibilidade para outros computadores usando o PNM na sub-rede local.</span><span class="sxs-lookup"><span data-stu-id="ed373-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="ed373-109">O usuário conectado deve optar por publicar seu apelido antes de ser anunciado.</span><span class="sxs-lookup"><span data-stu-id="ed373-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="ed373-110">O apelido é publicado na sub-rede usando a descoberta de serviços Web.</span><span class="sxs-lookup"><span data-stu-id="ed373-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="ed373-111">Além disso, objetos e aplicativos também podem ser publicados.</span><span class="sxs-lookup"><span data-stu-id="ed373-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="ed373-112">No entanto, o usuário deve especificar a publicação de objeto e aplicativo para os escopos '**pessoas ao meu redor**' ou '**todos**'.</span><span class="sxs-lookup"><span data-stu-id="ed373-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="ed373-113">Enumerador pessoas ao meu redor</span><span class="sxs-lookup"><span data-stu-id="ed373-113">People Near Me Enumerator</span></span>

<span data-ttu-id="ed373-114">O componente do enumerador pessoas ao meu redor enumera a lista de usuários na sub-rede local.</span><span class="sxs-lookup"><span data-stu-id="ed373-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="ed373-115">Usando essa lista, a descoberta de serviços da Web envia uma consulta de multicast e recebe as respostas.</span><span class="sxs-lookup"><span data-stu-id="ed373-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="ed373-116">Depois que a lista de apelidos é obtida, um aplicativo pode usar a API para recuperar mais dados sendo publicados pelo usuário (que é criptografado usando [Schannel](windows-vista-components-for-people-near-me.md)), como a lista de aplicativos registrados e todos os objetos que estão sendo publicados.</span><span class="sxs-lookup"><span data-stu-id="ed373-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="ed373-117">O processo de pesquisa e enumeração não ocorre automaticamente, mas deve ser iniciado explicitamente por um usuário ou um aplicativo entrando no PNM.</span><span class="sxs-lookup"><span data-stu-id="ed373-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="ed373-118">Os resultados da pesquisa são a lista de apelidos de outros usuários na mesma sub-rede que estão anunciando seus apelidos usando a API do PNM.</span><span class="sxs-lookup"><span data-stu-id="ed373-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="ed373-119">Gerenciador de publicação</span><span class="sxs-lookup"><span data-stu-id="ed373-119">Publication Manager</span></span>

<span data-ttu-id="ed373-120">O componente Gerenciador de publicação é responsável por publicar atualizações de presença, aplicativo ou objeto em contatos ou pessoas ao meu redor que são assinadas ou pesquisando dados.</span><span class="sxs-lookup"><span data-stu-id="ed373-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="ed373-121">Sinalização de pares</span><span class="sxs-lookup"><span data-stu-id="ed373-121">Peer Signaling</span></span>

<span data-ttu-id="ed373-122">O componente de sinalização de pares lida com a criação de conexões entre os pares para trocar dados.</span><span class="sxs-lookup"><span data-stu-id="ed373-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="ed373-123">Para pessoas ao meu redor, a sinalização de pares é usada quando um usuário ou aplicativo envia a consulta unicast para um computador específico para sua chave pública, aplicativos e objetos.</span><span class="sxs-lookup"><span data-stu-id="ed373-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="ed373-124">Receber manipulador de convite/UX</span><span class="sxs-lookup"><span data-stu-id="ed373-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="ed373-125">O componente manipulador de convite/UX de recebimento recebe um convite de entrada de outra pessoa, solicita que o usuário determine se deseja iniciar o aplicativo associado ao convite e, em seguida, inicia o aplicativo com base no usuário que está aceitando o convite.</span><span class="sxs-lookup"><span data-stu-id="ed373-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="ed373-126">Um convite é uma mensagem de outra pessoa para iniciar a atividade de colaboração usando um aplicativo específico que é instalado nos computadores do usuário e é anunciado pelo usuário que está sendo convidado.</span><span class="sxs-lookup"><span data-stu-id="ed373-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="ed373-127">Segurança do par</span><span class="sxs-lookup"><span data-stu-id="ed373-127">Peer Security</span></span>

<span data-ttu-id="ed373-128">Quando a presença, o aplicativo e o objeto são enviados, as informações são criptografadas usando um canal SSL ([Schannel](windows-vista-components-for-people-near-me.md)).</span><span class="sxs-lookup"><span data-stu-id="ed373-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="ed373-129">O computador inicial usa a chave pública do computador convidado para negociar uma chave secreta que é usada para criptografar os dados subsequentes enviados entre os dois pares.</span><span class="sxs-lookup"><span data-stu-id="ed373-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



