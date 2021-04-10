---
title: Interface IWMDRMSecurity
description: A interface IWMDRMSecurity gerencia uma variedade de informações relacionadas à segurança para o computador cliente e o subsistema DRM (gerenciamento de direitos digitais). Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Formato de mídia do Windows da interface IWMDRMSecurity
- Formato de mídia do Windows da interface IWMDRMSecurity, descrito
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293264"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="6b48f-105">Interface IWMDRMSecurity</span><span class="sxs-lookup"><span data-stu-id="6b48f-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="6b48f-106">A interface **IWMDRMSecurity** gerencia uma variedade de informações relacionadas à segurança para o computador cliente e o subsistema DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="6b48f-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="6b48f-107">Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="6b48f-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="6b48f-108">Passe **\_ IWMDRMSecurity IID** como o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="6b48f-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="6b48f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6b48f-109">Members</span></span>

<span data-ttu-id="6b48f-110">A interface **IWMDRMSecurity** herda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="6b48f-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="6b48f-111">**IWMDRMSecurity** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6b48f-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="6b48f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6b48f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6b48f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6b48f-113">Methods</span></span>

<span data-ttu-id="6b48f-114">A interface **IWMDRMSecurity** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6b48f-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="6b48f-115">Método</span><span class="sxs-lookup"><span data-stu-id="6b48f-115">Method</span></span>                                                                                      | <span data-ttu-id="6b48f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b48f-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b48f-117">**CheckCertForRevocation**</span><span class="sxs-lookup"><span data-stu-id="6b48f-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="6b48f-118">Determina se um certificado foi revogado.</span><span class="sxs-lookup"><span data-stu-id="6b48f-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="6b48f-119">**GetContentEnablersForRevocations**</span><span class="sxs-lookup"><span data-stu-id="6b48f-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="6b48f-120">Recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados revogados.</span><span class="sxs-lookup"><span data-stu-id="6b48f-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="6b48f-121">**GetContentEnablersFromHashes**</span><span class="sxs-lookup"><span data-stu-id="6b48f-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="6b48f-122">Recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados com hash.</span><span class="sxs-lookup"><span data-stu-id="6b48f-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="6b48f-123">**GetMachineCertificate**</span><span class="sxs-lookup"><span data-stu-id="6b48f-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="6b48f-124">Recupera o certificado do computador do subsistema DRM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="6b48f-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="6b48f-125">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="6b48f-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="6b48f-126">Recupera uma lista de certificados revogados do repositório local.</span><span class="sxs-lookup"><span data-stu-id="6b48f-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="6b48f-127">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="6b48f-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="6b48f-128">Recupera o número de versão de uma lista de certificados revogados no repositório local.</span><span class="sxs-lookup"><span data-stu-id="6b48f-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="6b48f-129">**GetSecurityVersion**</span><span class="sxs-lookup"><span data-stu-id="6b48f-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="6b48f-130">Recupera a versão do subsistema DRM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="6b48f-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="6b48f-131">**PerformSecurityUpdate**</span><span class="sxs-lookup"><span data-stu-id="6b48f-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="6b48f-132">Inicia uma atualização de segurança para o subsistema DRM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="6b48f-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="6b48f-133">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="6b48f-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="6b48f-134">Define uma lista de certificados revogados no repositório local.</span><span class="sxs-lookup"><span data-stu-id="6b48f-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="6b48f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b48f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b48f-136">**Exemplo de individualização de DRM**</span><span class="sxs-lookup"><span data-stu-id="6b48f-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="6b48f-137">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="6b48f-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6b48f-138">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="6b48f-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





