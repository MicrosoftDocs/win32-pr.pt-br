---
title: Propriedade TaskSettings. NetworkSettings
description: Para scripts, Obtém ou define o objeto de configurações de rede que contém um nome e identificador de perfil de rede.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Agendador de Tarefas da propriedade NetworkSettings
- Propriedade NetworkSettings Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644381"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="8abfd-106">Propriedade TaskSettings. NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="8abfd-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="8abfd-107">Para scripts, Obtém ou define o objeto de configurações de rede que contém um nome e identificador de perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="8abfd-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="8abfd-108">Se a propriedade [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) for **true** e um propfile de rede for especificado na propriedade **NetworkSettings** , a tarefa será executada somente se o perfil de rede especificado estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="8abfd-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="8abfd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8abfd-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="8abfd-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8abfd-110">Property value</span></span>

<span data-ttu-id="8abfd-111">Um objeto [**NetworkSettings**](networksettings.md) que contém um identificador e nome de perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="8abfd-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="8abfd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8abfd-112">Requirements</span></span>



| <span data-ttu-id="8abfd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8abfd-113">Requirement</span></span> | <span data-ttu-id="8abfd-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8abfd-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8abfd-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8abfd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8abfd-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8abfd-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8abfd-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8abfd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8abfd-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8abfd-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8abfd-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8abfd-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="8abfd-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8abfd-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8abfd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8abfd-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8abfd-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8abfd-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8abfd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8abfd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8abfd-124">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="8abfd-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="8abfd-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="8abfd-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





