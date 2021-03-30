---
description: Descreve as configurações de política de energia que compõem um esquema de energia.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Configurações de política de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662179"
---
# <a name="power-policy-settings"></a><span data-ttu-id="4d4e5-103">Configurações de política de energia</span><span class="sxs-lookup"><span data-stu-id="4d4e5-103">Power Policy Settings</span></span>

<span data-ttu-id="4d4e5-104">Planos de energia e esquemas consistem em preferências e configurações de política.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="4d4e5-105">Um plano de energia consiste em um grupo de preferências de configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="4d4e5-106">Essas preferências consistem em um valor AC e DC para cada uma das configurações de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="4d4e5-107">Cada plano de energia é identificado por meio de um **GUID** exclusivo, bem como um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="4d4e5-108">O Windows Vista tem três planos de energia padrão: economia de energia, equilibrado e alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="4d4e5-109">Esses planos podem ser personalizados e planos adicionais podem ser criados.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="4d4e5-110">Todos os planos de energia têm um atributo de personalidade que indica o comportamento de economia de energia geral do plano.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="4d4e5-111">A tabela a seguir mostra os três personalidades do plano de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="4d4e5-112">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="4d4e5-112">Display name</span></span>     | <span data-ttu-id="4d4e5-113">Description</span><span class="sxs-lookup"><span data-stu-id="4d4e5-113">Description</span></span>                                                                   | <span data-ttu-id="4d4e5-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="4d4e5-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="4d4e5-115">Economia de energia</span><span class="sxs-lookup"><span data-stu-id="4d4e5-115">Power Saver</span></span>      | <span data-ttu-id="4d4e5-116">Oferece um desempenho reduzido que pode aumentar a economia de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="4d4e5-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="4d4e5-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="4d4e5-118">Balanced</span><span class="sxs-lookup"><span data-stu-id="4d4e5-118">Balanced</span></span>         | <span data-ttu-id="4d4e5-119">Balanceia automaticamente o consumo de energia e de desempenho de acordo com a demanda.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="4d4e5-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="4d4e5-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="4d4e5-121">Alto Desempenho</span><span class="sxs-lookup"><span data-stu-id="4d4e5-121">High Performance</span></span> | <span data-ttu-id="4d4e5-122">Oferece desempenho máximo às custas de maior consumo de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="4d4e5-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="4d4e5-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="4d4e5-124">Os dispositivos que dão suporte ao modo de [espera moderno](/windows-hardware/design/device-experiences/modern-standby) só permitem o plano de energia **equilibrado** .</span><span class="sxs-lookup"><span data-stu-id="4d4e5-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="4d4e5-125">O **modo de espera moderno** é a solução mais recente e mais simplificada para o gerenciamento de configurações de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="4d4e5-126">Cada computador tem um plano de energia único e ativo.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="4d4e5-127">Por padrão, os usuários sem privilégios são capazes de acessar as configurações de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="4d4e5-128">O acesso a todas as configurações de energia individuais pode ser controlado por meio de ACLs nas configurações de energia ou por meio de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="4d4e5-129">Os aplicativos devem chamar [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) para determinar se o usuário tem acesso à configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="4d4e5-130">Cada configuração de energia é identificada por um **GUID** exclusivo e inclui um nome amigável, descrição, valores permitidos e valores padrão para AC e DC.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="4d4e5-131">As configurações de energia personalizadas podem ser criadas usando a função [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .</span><span class="sxs-lookup"><span data-stu-id="4d4e5-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d4e5-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d4e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d4e5-133">Esquemas de energia</span><span class="sxs-lookup"><span data-stu-id="4d4e5-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
