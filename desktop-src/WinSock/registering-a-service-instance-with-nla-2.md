---
description: Os clientes de NLA podem gravar informações de configuração de rede em todo o sistema, permitindo que consultas futuras retornem as informações de configuração especificadas, independentemente de a rede estar ativa.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrando uma instância de serviço com NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783766"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="cc943-103">Registrando uma instância de serviço com NLA</span><span class="sxs-lookup"><span data-stu-id="cc943-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="cc943-104">Os clientes de NLA podem gravar informações de configuração de rede em todo o sistema, permitindo que consultas futuras retornem as informações de configuração especificadas, independentemente de a rede estar ativa.</span><span class="sxs-lookup"><span data-stu-id="cc943-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="cc943-105">Essa funcionalidade permite que os clientes de NLA afetem uma experiência de usuário consistente de informações de rede em vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cc943-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc943-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc943-106">Parameters</span></span>

<span data-ttu-id="cc943-107">Para registrar uma instância de serviço com o provedor de serviços de reconhecimento de local de rede, use a função [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) .</span><span class="sxs-lookup"><span data-stu-id="cc943-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="cc943-108">Para registrar corretamente uma instância de serviço, determinados parâmetros da função **WSASetService** devem ser definidos com as informações apropriadas, conforme explicado nesta seção.</span><span class="sxs-lookup"><span data-stu-id="cc943-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="cc943-109">Para referência rápida, a função **WSASetService** tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="cc943-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="cc943-110">Para o parâmetro *lpqsRegInfo* , forneça uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) de um resultado de consulta NLA SP ou tenha construído a adesão aos requisitos de uma consulta NLA SP, conforme especificado em [consultando NLA](querying-nla-2.md).</span><span class="sxs-lookup"><span data-stu-id="cc943-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="cc943-111">As operações com suporte para o parâmetro *essOperation* são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="cc943-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="cc943-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>registro de RNRSERVICE \_</span><span class="sxs-lookup"><span data-stu-id="cc943-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="cc943-113">A rede definida na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecida no *lpqsRegInfo* torna-se persistente para o usuário ativo, armazenando a instância de rede no hive do registro para o usuário atual, o que permite a representação.</span><span class="sxs-lookup"><span data-stu-id="cc943-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="cc943-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ excluir</span><span class="sxs-lookup"><span data-stu-id="cc943-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="cc943-115">Se a rede definida na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecida em *lpqsRegInfo* for persistente, ela será removida.</span><span class="sxs-lookup"><span data-stu-id="cc943-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="cc943-116">A operação especificada no parâmetro *essOperation* pode ser modificada pelas seguintes opções, que podem ser especificadas com binary ou Logic:</span><span class="sxs-lookup"><span data-stu-id="cc943-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="cc943-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nome amigável de NLA \_</span><span class="sxs-lookup"><span data-stu-id="cc943-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="cc943-118">Quando usado com o \_ registro RNRSERVICE, o campo *lpszComment* da rede definida em *lpqsRegInfo* é verificado quanto à validade e armazenado de forma persistente.</span><span class="sxs-lookup"><span data-stu-id="cc943-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="cc943-119">Quando usado com RNRSERVICE \_ Delete e a rede definida tem um nome amigável, o nome amigável é removido, mas a entrada de rede permanece intacta.</span><span class="sxs-lookup"><span data-stu-id="cc943-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="cc943-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_rede NLA AllUsers \_</span><span class="sxs-lookup"><span data-stu-id="cc943-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="cc943-121">Quando usado com o \_ registro RNRSERVICE, a entrada é armazenada de forma persistente em hKey \_ local \_ Machine, disponibilizando-a durante consultas a todos os usuários no computador local.</span><span class="sxs-lookup"><span data-stu-id="cc943-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="cc943-122">Quando usado com RNRSERVICE \_ delete, a rede especificada é removida da \_ máquina local hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="cc943-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="cc943-123">Um erro será retornado se a rede especificada não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="cc943-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="cc943-124">Para excluir uma rede do hive do registro do usuário atual, esse sinalizador não deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="cc943-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="cc943-125">Esse sinalizador só é válido no contexto de segurança de um administrador do sistema local.</span><span class="sxs-lookup"><span data-stu-id="cc943-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="cc943-126">O NLA dá suporte aos seguintes códigos de erro para chamadas de função [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="cc943-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="cc943-127">Erro</span><span class="sxs-lookup"><span data-stu-id="cc943-127">Error</span></span>             | <span data-ttu-id="cc943-128">Significado</span><span class="sxs-lookup"><span data-stu-id="cc943-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc943-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="cc943-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="cc943-130">Uma chamada bem-sucedida para a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar o NLA não foi executada.</span><span class="sxs-lookup"><span data-stu-id="cc943-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="cc943-131">WSAEACCESS</span><span class="sxs-lookup"><span data-stu-id="cc943-131">WSAEACCESS</span></span>        | <span data-ttu-id="cc943-132">\_ \_ A rede de NLA AllUsers foi especificada em *dwControlFlags* , embora não esteja no contexto de segurança de um administrador de sistema local.</span><span class="sxs-lookup"><span data-stu-id="cc943-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="cc943-133">WSAEALREADY</span><span class="sxs-lookup"><span data-stu-id="cc943-133">WSAEALREADY</span></span>       | <span data-ttu-id="cc943-134">A rede especificada já está armazenada de forma persistente na maneira solicitada e nenhum sinalizador foi especificado em *dwControlFlags* para indicar uma atualização para a entrada existente.</span><span class="sxs-lookup"><span data-stu-id="cc943-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="cc943-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="cc943-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="cc943-136">Uma família de protocolos foi especificada para a qual não há suporte.</span><span class="sxs-lookup"><span data-stu-id="cc943-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="cc943-137">Somente as famílias de protocolo IP têm suporte no NLA.</span><span class="sxs-lookup"><span data-stu-id="cc943-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="cc943-138">WSAEPFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="cc943-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="cc943-139">Um protocolo foi especificado para o qual não há suporte.</span><span class="sxs-lookup"><span data-stu-id="cc943-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="cc943-140">Somente o protocolo IP tem suporte em NLA.</span><span class="sxs-lookup"><span data-stu-id="cc943-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



