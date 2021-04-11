---
title: Interface IWMDRMLicenseManagement
description: A interface IWMDRMLicenseManagement fornece métodos que executam operações gerais relacionadas ao armazenamento de licença local. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMLICENSEMANAGEMENT IID como o parâmetro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Formato de mídia do Windows da interface IWMDRMLicenseManagement
- Formato de mídia do Windows da interface IWMDRMLicenseManagement, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293173"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="c1bcb-106">Interface IWMDRMLicenseManagement</span><span class="sxs-lookup"><span data-stu-id="c1bcb-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="c1bcb-107">A interface **IWMDRMLicenseManagement** fornece métodos que executam operações gerais relacionadas ao armazenamento de licença local.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="c1bcb-108">Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="c1bcb-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="c1bcb-109">Passe **\_ IWMDRMLicenseManagement IID** como o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="c1bcb-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="c1bcb-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c1bcb-110">Members</span></span>

<span data-ttu-id="c1bcb-111">A interface **IWMDRMLicenseManagement** herda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="c1bcb-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="c1bcb-112">**IWMDRMLicenseManagement** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1bcb-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="c1bcb-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1bcb-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c1bcb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1bcb-114">Methods</span></span>

<span data-ttu-id="c1bcb-115">A interface **IWMDRMLicenseManagement** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="c1bcb-116">Método</span><span class="sxs-lookup"><span data-stu-id="c1bcb-116">Method</span></span>                                                                                               | <span data-ttu-id="c1bcb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1bcb-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1bcb-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="c1bcb-119">Adquire de forma assíncrona uma licença de uma URL especificada.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="c1bcb-120">**BackupLicenses**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="c1bcb-121">Cria um backup das licenças no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="c1bcb-122">**CleanLicenseStore**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="c1bcb-123">Remove as licenças marcadas do repositório de licenças e desfragmenta o armazenamento para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="c1bcb-124">**CreateLicenseEnumeration**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="c1bcb-125">Cria um objeto enumerador de licenças populado com informações de licença com base em valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="c1bcb-126">**CreateLicenseRevocationChallenge**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="c1bcb-127">Gera um desafio de revogação de licença.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="c1bcb-128">**DeleteLicense**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="c1bcb-129">Exclui uma licença do armazenamento de licença local temporário.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="c1bcb-130">**MonitorLicenseAcquisition**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="c1bcb-131">Inicia o monitoramento de um processo de aquisição de licença.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="c1bcb-132">**ProcessLicenseDeletionMessage**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="c1bcb-133">Exclui uma licença que foi importada para o conteúdo originalmente protegido com outro sistema de proteção de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="c1bcb-134">**ProcessLicenseRevocationResponse**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="c1bcb-135">Revoga licenças do repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="c1bcb-136">**RestoreLicenses**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="c1bcb-137">Restaura as licenças de backup anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="c1bcb-138">**StoreLicense**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="c1bcb-139">Adiciona uma licença ao repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="c1bcb-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="c1bcb-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1bcb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1bcb-141">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c1bcb-142">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="c1bcb-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





