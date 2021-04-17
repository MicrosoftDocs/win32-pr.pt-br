---
description: Durante a inicialização do sistema, o SCM inicia todos os serviços de início automático e os serviços dos quais eles dependem. Por exemplo, se um serviço de início automático depender de um serviço de início de demanda, o serviço de início de demanda também será iniciado automaticamente.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Iniciando serviços automaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762895"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="d03ef-104">Iniciando serviços automaticamente</span><span class="sxs-lookup"><span data-stu-id="d03ef-104">Automatically Starting Services</span></span>

<span data-ttu-id="d03ef-105">Durante a inicialização do sistema, o SCM inicia todos os serviços de início automático e os serviços dos quais eles dependem.</span><span class="sxs-lookup"><span data-stu-id="d03ef-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="d03ef-106">Por exemplo, se um serviço de início automático depender de um serviço de início de demanda, o serviço de início de demanda também será iniciado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d03ef-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="d03ef-107">A ordem de carregamento é determinada pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="d03ef-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="d03ef-108">A ordem dos grupos na lista de grupos de ordenação de carregamento.</span><span class="sxs-lookup"><span data-stu-id="d03ef-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="d03ef-109">Essas informações são armazenadas no valor **ServiceGroupOrder** na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="d03ef-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="d03ef-110">**HKEY \_ \_ computador local \\ sistema \\ CurrentControlSet \\ Control**</span><span class="sxs-lookup"><span data-stu-id="d03ef-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="d03ef-111">Para especificar o grupo de ordenação de carga para um serviço, use o parâmetro *lpLoadOrderGroup* da função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="d03ef-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="d03ef-112">A ordem dos serviços dentro de um grupo especificado no vetor de ordem de marcas.</span><span class="sxs-lookup"><span data-stu-id="d03ef-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="d03ef-113">Essas informações são armazenadas no valor **GroupOrderList** na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="d03ef-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="d03ef-114">**HKEY \_ \_ computador local \\ sistema \\ CurrentControlSet \\ Control**</span><span class="sxs-lookup"><span data-stu-id="d03ef-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="d03ef-115">As dependências listadas para cada serviço.</span><span class="sxs-lookup"><span data-stu-id="d03ef-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="d03ef-116">Quando a inicialização for concluída, o sistema executará o programa de verificação de inicialização especificado pelo valor **BootVerificationProgram** da seguinte chave do registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control**.</span><span class="sxs-lookup"><span data-stu-id="d03ef-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="d03ef-117">Por padrão, esse valor não é definido.</span><span class="sxs-lookup"><span data-stu-id="d03ef-117">By default, this value is not set.</span></span> <span data-ttu-id="d03ef-118">O sistema simplesmente relata que a inicialização foi bem-sucedida depois que o primeiro usuário fez logon.</span><span class="sxs-lookup"><span data-stu-id="d03ef-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="d03ef-119">Você pode fornecer um programa de verificação de inicialização que verifica o sistema em busca de problemas e relata o status de inicialização para o SCM usando a função [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="d03ef-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="d03ef-120">Após uma inicialização bem-sucedida, o sistema salva um clone do banco de dados na última configuração válida (LKG).</span><span class="sxs-lookup"><span data-stu-id="d03ef-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="d03ef-121">O sistema pode restaurar essa cópia do banco de dados se as alterações feitas no banco de dados ativo causarem a falha da reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="d03ef-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="d03ef-122">A seguir está a chave do registro para este banco de dados:</span><span class="sxs-lookup"><span data-stu-id="d03ef-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="d03ef-123">**HKEY \_ local \_ Machine \\ Control do sistema de \\ controle *xxx* \\ serviços**</span><span class="sxs-lookup"><span data-stu-id="d03ef-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="d03ef-124">em que *xxx* é o valor salvo no seguinte valor de registro: **HKEY \_ local \_ Machine \\ System \\ selecione \\ LastKnownGood**.</span><span class="sxs-lookup"><span data-stu-id="d03ef-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="d03ef-125">Se um serviço de início automático com um erro de serviço \_ \_ crítico não for iniciado, o SCM reinicializará o computador usando a configuração LKG.</span><span class="sxs-lookup"><span data-stu-id="d03ef-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="d03ef-126">Se a configuração LKG já estiver sendo usada, a inicialização falhará.</span><span class="sxs-lookup"><span data-stu-id="d03ef-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="d03ef-127">Um serviço de início automático pode ser configurado como um serviço de início automático atrasado chamando a função [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) com informações de \_ \_ início automático atrasadas de configuração de serviço \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d03ef-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="d03ef-128">Essa alteração entra em vigor após a próxima inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="d03ef-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="d03ef-129">Para obter mais informações, [**consulte \_ \_ informações de \_ início \_ automático com atraso no serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span><span class="sxs-lookup"><span data-stu-id="d03ef-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



