---
description: A propriedade AVAILABLEFREEREG especifica, em quilobytes, o total de espaço livre disponível no registro depois de chamar a ação AllocateRegistrySpace. O valor máximo da propriedade AVAILABLEFREEREG é de 2 milhões quilobytes. Essa propriedade é definida somente no Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propriedade AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748990"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="5e9b6-103">Propriedade AVAILABLEFREEREG</span><span class="sxs-lookup"><span data-stu-id="5e9b6-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="5e9b6-104">A propriedade **AVAILABLEFREEREG** especifica, em quilobytes, o total de espaço livre disponível no registro depois de chamar a [ação AllocateRegistrySpace](allocateregistryspace-action.md).</span><span class="sxs-lookup"><span data-stu-id="5e9b6-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="5e9b6-105">O valor máximo da propriedade **AVAILABLEFREEREG** é de 2 milhões quilobytes.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="5e9b6-106">Essa propriedade é definida somente no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9b6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e9b6-107">Remarks</span></span>

<span data-ttu-id="5e9b6-108">A propriedade **AVAILABLEFREEREG** deve ser definida com um valor grande o suficiente para garantir espaço suficiente no registro para todas as informações de Registro adicionadas pela instalação.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="5e9b6-109">O valor mínimo necessário para garantir espaço suficiente depende de onde a [ação AllocateRegistrySpace](allocateregistryspace-action.md) está localizada na sequência de ações, pois o instalador aumenta automaticamente o espaço conforme necessário ao registrar informações nas tabelas [registro](registry-table.md), [classe](class-table.md), [selfreg](selfreg-table.md), [extensão](extension-table.md), [MIME](mime-table.md)e [verbo](verb-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5e9b6-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="5e9b6-110">O instalador não aumenta o espaço total do registro para o valor especificado por **AVAILABLEFREEREG** até chegar a AllocateRegistrySpace na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="5e9b6-111">Se AllocateRegistrySpace for uma das primeiras ações na sequência de ação, **AVAILABLEFREEREG** deverá ser definido como o espaço total exigido pelas informações de registro na tabela do registro, na tabela de classes, na tabela de typelib, na tabela selfreg, na tabela de extensão, na tabela de MIME, na tabela de verbos, no registro de [ações personalizadas](custom-actions.md) , no auto-registro e em qualquer outra informação de registro gravada durante a instalação</span><span class="sxs-lookup"><span data-stu-id="5e9b6-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="5e9b6-112">O valor de **AVAILABLEFREEREG** é a quantidade total de informações adicionadas pela instalação e garante espaço suficiente em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="5e9b6-113">Esse também é o caso mais comum.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-113">This is also the most common case.</span></span>

<span data-ttu-id="5e9b6-114">Se a ação AllocateRegistrySpace puder ser criada na sequência de ação após todas as [ações padrão](standard-actions.md) que gravam dados de registro, como [WriteRegistryValues](writeregistryvalues-action.md) e [RegisterClassInfo](registerclassinfo-action.md), o valor de **AVAILABLEFREEREG** precisará ser definido apenas como o espaço necessário para registrar ações personalizadas, registrar bibliotecas de tipos e quaisquer outras informações ainda não registradas por meio das tabelas.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9b6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e9b6-115">Requirements</span></span>



| <span data-ttu-id="5e9b6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9b6-116">Requirement</span></span> | <span data-ttu-id="5e9b6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5e9b6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9b6-118">Versão</span><span class="sxs-lookup"><span data-stu-id="5e9b6-118">Version</span></span><br/> | <span data-ttu-id="5e9b6-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5e9b6-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5e9b6-121">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5e9b6-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5e9b6-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e9b6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e9b6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9b6-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e9b6-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




