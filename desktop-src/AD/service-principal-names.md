---
title: Nomes de Entidade de Serviço
description: Um SPN (nome da entidade de serviço) é um identificador exclusivo de uma instância de serviço.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nomes de Entidade de Serviço
- SPN consulte nomes da entidade de serviço
- ANÚNCIO do nome da entidade de serviço
- ANÚNCIO do nome da entidade de serviço, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823629"
---
# <a name="service-principal-names"></a><span data-ttu-id="c8714-107">Nomes de Entidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="c8714-107">Service Principal Names</span></span>

<span data-ttu-id="c8714-108">Um SPN (nome da entidade de serviço) é um identificador exclusivo de uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="c8714-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="c8714-109">Os SPNs são usados pela [autenticação Kerberos](mutual-authentication-using-kerberos.md) para associar uma instância de serviço a uma conta de logon de serviço.</span><span class="sxs-lookup"><span data-stu-id="c8714-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="c8714-110">Isso permite que um aplicativo cliente solicite que o serviço autentique uma conta mesmo que o cliente não tenha o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="c8714-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="c8714-111">Se você instalar várias instâncias de um serviço em computadores em uma floresta, cada instância deverá ter seu próprio SPN.</span><span class="sxs-lookup"><span data-stu-id="c8714-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="c8714-112">Uma determinada instância de serviço pode ter vários SPNs se houver vários nomes que os clientes podem usar para autenticação.</span><span class="sxs-lookup"><span data-stu-id="c8714-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="c8714-113">Por exemplo, um SPN sempre inclui o nome do computador host no qual a instância de serviço está em execução, portanto, uma instância de serviço pode registrar um SPN para cada nome ou alias de seu host.</span><span class="sxs-lookup"><span data-stu-id="c8714-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="c8714-114">Para obter mais informações sobre o formato SPN e compor um SPN exclusivo, consulte [formatos de nome para SPNs exclusivos](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="c8714-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="c8714-115">Antes que o serviço de autenticação Kerberos possa usar um SPN para autenticar um serviço, o SPN deve ser registrado no objeto de conta que a instância de serviço usa para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="c8714-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="c8714-116">Um determinado SPN pode ser registrado em apenas uma conta.</span><span class="sxs-lookup"><span data-stu-id="c8714-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="c8714-117">Para serviços Win32, um instalador de serviço especifica a conta de logon quando uma instância do serviço é instalada.</span><span class="sxs-lookup"><span data-stu-id="c8714-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="c8714-118">Em seguida, o instalador compõe os SPNs e os grava como uma propriedade do objeto Account no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c8714-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="c8714-119">Se a conta de logon de uma instância de serviço for alterada, os SPNs deverão ser registrados novamente na nova conta.</span><span class="sxs-lookup"><span data-stu-id="c8714-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="c8714-120">Para obter mais informações, consulte [como um serviço registra seus SPNs](how-a-service-registers-its-spns.md).</span><span class="sxs-lookup"><span data-stu-id="c8714-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="c8714-121">Quando um cliente deseja se conectar a um serviço, ele localiza uma instância do serviço, compõe um SPN para essa instância, conecta-se ao serviço e apresenta o SPN para autenticação do serviço.</span><span class="sxs-lookup"><span data-stu-id="c8714-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="c8714-122">Para obter mais informações, consulte [como os clientes compõem o SPN de um serviço](how-clients-compose-a-serviceampaposs-spn.md).</span><span class="sxs-lookup"><span data-stu-id="c8714-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c8714-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c8714-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c8714-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c8714-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c8714-125">Formatos de nome para SPNs exclusivos</span><span class="sxs-lookup"><span data-stu-id="c8714-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="c8714-126">Como um serviço compõe seus SPNs</span><span class="sxs-lookup"><span data-stu-id="c8714-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="c8714-127">Como um serviço registra seus SPNs</span><span class="sxs-lookup"><span data-stu-id="c8714-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="c8714-128">Como os clientes compõem o SPN de um serviço</span><span class="sxs-lookup"><span data-stu-id="c8714-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="c8714-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8714-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8714-130">O que é um SPN e por que você deve se importar?</span><span class="sxs-lookup"><span data-stu-id="c8714-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="c8714-131">Autenticação mútua usando Kerberos</span><span class="sxs-lookup"><span data-stu-id="c8714-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 