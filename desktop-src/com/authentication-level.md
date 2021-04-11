---
title: Nível de autenticação
description: O nível de autenticação controla a quantidade de segurança que um cliente ou servidor deseja de seu SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292849"
---
# <a name="authentication-level"></a><span data-ttu-id="80182-103">Nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="80182-103">Authentication Level</span></span>

<span data-ttu-id="80182-104">O nível de autenticação controla a quantidade de segurança que um cliente ou servidor deseja de seu SSP.</span><span class="sxs-lookup"><span data-stu-id="80182-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="80182-105">O nível de autenticação é definido passando um \_ valor xxx de nível de autenticação RPC C apropriado \_ \_ \_ para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) por meio do parâmetro *dwAuthnLevel* .</span><span class="sxs-lookup"><span data-stu-id="80182-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="80182-106">Os níveis de autenticação do cliente e do servidor são comparados durante o handshake, e a configuração de proteção de segurança de nível superior é usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="80182-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="80182-107">Os diferentes níveis de autenticação são descritos da seguinte maneira, da proteção de segurança de nível mais baixo para a mais alta:</span><span class="sxs-lookup"><span data-stu-id="80182-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="80182-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Nenhum (RPC \_ C \_ Authn \_ nível \_ nenhum)</span><span class="sxs-lookup"><span data-stu-id="80182-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="80182-109">Nenhuma autenticação é executada durante a comunicação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="80182-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="80182-110">Todas as configurações de segurança são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="80182-110">All security settings are ignored.</span></span> <span data-ttu-id="80182-111">Esse nível de autenticação poderá ser definido somente se o [nível de serviço de autenticação](com-authentication-service-constants.md) for RPC \_ C \_ Authn \_ None.</span><span class="sxs-lookup"><span data-stu-id="80182-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="80182-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Padrão ( \_ padrão de \_ nível de autenticação RPC C \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="80182-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="80182-113">COM escolhe o nível de autenticação usando sua negociação de cobertura de segurança normal.</span><span class="sxs-lookup"><span data-stu-id="80182-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="80182-114">Ele nunca escolherá um nível de autenticação de nenhum.</span><span class="sxs-lookup"><span data-stu-id="80182-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="80182-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Conectar ( \_ conexão em \_ nível de autenticação RPC C \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="80182-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="80182-116">O handshake de autenticação normal ocorre entre o cliente e o servidor, e uma chave de sessão é estabelecida, mas essa chave nunca é usada para comunicação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="80182-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="80182-117">Toda a comunicação após o handshake não é segura.</span><span class="sxs-lookup"><span data-stu-id="80182-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="80182-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Chamada ( \_ chamada de \_ nível de autenticação RPC C \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="80182-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="80182-119">Somente os cabeçalhos do início de cada chamada são assinados.</span><span class="sxs-lookup"><span data-stu-id="80182-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="80182-120">O restante dos dados trocados entre o cliente e o servidor não é assinado nem criptografado.</span><span class="sxs-lookup"><span data-stu-id="80182-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="80182-121">A maioria dos SSPs não dá suporte a esse nível de autenticação e o promove silenciosamente para o pacote.</span><span class="sxs-lookup"><span data-stu-id="80182-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="80182-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Pacote (RPC \_ C \_ Authn \_ nível \_ PKT)</span><span class="sxs-lookup"><span data-stu-id="80182-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="80182-123">O cabeçalho de cada pacote é assinado, mas não criptografado.</span><span class="sxs-lookup"><span data-stu-id="80182-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="80182-124">Os próprios pacotes não são assinados ou criptografados.</span><span class="sxs-lookup"><span data-stu-id="80182-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="80182-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integridade do pacote ( \_ integridade do PCT do nível de autenticação RPC C \_ \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="80182-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="80182-126">Cada pacote de dados é assinado em sua totalidade, mas não é criptografado.</span><span class="sxs-lookup"><span data-stu-id="80182-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="80182-127">Como todos os dados são assinados pelo remetente, o destinatário pode ter certeza de que nenhum dos dados foi adulterado durante o trânsito.</span><span class="sxs-lookup"><span data-stu-id="80182-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="80182-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacidade de pacote ( \_ privacidade do PCT do nível de autenticação RPC C \_ \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="80182-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="80182-129">Cada pacote de dados é assinado e criptografado.</span><span class="sxs-lookup"><span data-stu-id="80182-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="80182-130">Isso ajuda a proteger toda a comunicação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="80182-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="80182-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80182-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80182-132">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="80182-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="80182-133">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="80182-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




