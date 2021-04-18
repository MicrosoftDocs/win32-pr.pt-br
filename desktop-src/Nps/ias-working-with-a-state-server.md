---
title: Trabalhando com um servidor de estado
description: O NPS executa a autenticação usando um banco de dados configurado no site do servidor NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760406"
---
# <a name="working-with-a-state-server"></a><span data-ttu-id="b75d1-103">Trabalhando com um servidor de estado</span><span class="sxs-lookup"><span data-stu-id="b75d1-103">Working With a State Server</span></span>

> [!Note]  
> <span data-ttu-id="b75d1-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b75d1-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="b75d1-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="b75d1-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="b75d1-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="b75d1-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="b75d1-107">O NPS executa a autenticação usando um banco de dados configurado no site do servidor NPS.</span><span class="sxs-lookup"><span data-stu-id="b75d1-107">NPS performs authentication using a database that is configured at the NPS server site.</span></span> <span data-ttu-id="b75d1-108">Esse banco de dados de autenticação pode ser o banco de dados do usuário para um domínio do Windows ou pode ser desenhado sobre as informações do usuário obtidas do Windows Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b75d1-108">This authentication database could be the user database for a Windows Domain or it could draw upon the user information obtained from the Windows Active Directory.</span></span> <span data-ttu-id="b75d1-109">O diagrama a seguir ilustra uma configuração típica que mostra como o NPS interage com bancos de dados de autenticação como, por exemplo, um usuário de domínio do Windows ou Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b75d1-109">The following diagram illustrates a typical configuration that shows how NPS interacts with authentication databases such as a Windows Domain user database or Active Directory.</span></span> <span data-ttu-id="b75d1-110">O diagrama também mostra como o NPS pode interagir com um servidor de estado que é fornecido por terceiros.</span><span class="sxs-lookup"><span data-stu-id="b75d1-110">The diagram also shows how NPS could interact with a state server that is provided by a third party.</span></span> <span data-ttu-id="b75d1-111">A principal finalidade de um servidor de estado é limitar o número de sessões de logon simultâneas que um único usuário pode executar.</span><span class="sxs-lookup"><span data-stu-id="b75d1-111">The primary purpose of a state server is to limit the number of simultaneous logon sessions a single user can run.</span></span>

![NPS interagindo com servidor de estado e bancos de dados de autenticação](images/ias02.png)

<span data-ttu-id="b75d1-113">Há dois pontos de interação entre o NPS e o servidor de estado.</span><span class="sxs-lookup"><span data-stu-id="b75d1-113">There are two points of interaction between NPS and the state server.</span></span> <span data-ttu-id="b75d1-114">Ocorre uma interação quando o NPS recebe uma solicitação de autenticação do NAS.</span><span class="sxs-lookup"><span data-stu-id="b75d1-114">One interaction takes place when NPS receives an authentication request from the NAS.</span></span> <span data-ttu-id="b75d1-115">O servidor de estado fornece informações de seu banco de dados para determinar se deseja aceitar ou negar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b75d1-115">The state server provides information from its database to determine whether to accept or deny the request.</span></span> <span data-ttu-id="b75d1-116">A outra interação ocorre quando o NPS recebe solicitações de contabilização do NAS.</span><span class="sxs-lookup"><span data-stu-id="b75d1-116">The other interaction takes place when NPS receives accounting requests from the NAS.</span></span> <span data-ttu-id="b75d1-117">O servidor de estado usa o formulário de informações dessas solicitações de contabilidade para atualizar seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b75d1-117">The state server uses the information form these accounting requests to update its database.</span></span>

<span data-ttu-id="b75d1-118">Para obter mais informações sobre servidores de estado, consulte:</span><span class="sxs-lookup"><span data-stu-id="b75d1-118">For more information on state servers see:</span></span>

-   [<span data-ttu-id="b75d1-119">Considerações de design de servidor de estado</span><span class="sxs-lookup"><span data-stu-id="b75d1-119">State Server Design Considerations</span></span>](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a><span data-ttu-id="b75d1-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b75d1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b75d1-121">Serviço de autenticação da Internet e servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="b75d1-121">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="b75d1-122">Autenticação, autorização e contabilização RADIUS</span><span class="sxs-lookup"><span data-stu-id="b75d1-122">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="b75d1-123">Registrando em log com o servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="b75d1-123">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 