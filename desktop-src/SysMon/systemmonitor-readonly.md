---
title: Propriedade SystemMonitor. ReadOnly
description: Recupera ou define um valor que determina se um usuário pode modificar os valores de Propriedade do controle.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Propriedade ReadOnly do SysMon
- Propriedade ReadOnly SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918408"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="3ca40-106">Propriedade SystemMonitor. ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3ca40-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="3ca40-107">Recupera ou define um valor que determina se um usuário pode modificar os valores de Propriedade do controle.</span><span class="sxs-lookup"><span data-stu-id="3ca40-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="3ca40-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3ca40-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca40-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ca40-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3ca40-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3ca40-110">Property value</span></span>

<span data-ttu-id="3ca40-111">True se você não quiser que o usuário modifique os valores de Propriedade do controle; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="3ca40-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="3ca40-112">O valor padrão é false, o que significa que os usuários podem modificar os valores de Propriedade do controle.</span><span class="sxs-lookup"><span data-stu-id="3ca40-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca40-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ca40-113">Remarks</span></span>

<span data-ttu-id="3ca40-114">Quando o valor dessa propriedade for true, as seguintes condições estarão em vigor:</span><span class="sxs-lookup"><span data-stu-id="3ca40-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="3ca40-115">O usuário não pode usar o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="3ca40-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="3ca40-116">Os seguintes botões da barra de ferramentas estão desabilitados:</span><span class="sxs-lookup"><span data-stu-id="3ca40-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="3ca40-117">Novo conjunto de contadores</span><span class="sxs-lookup"><span data-stu-id="3ca40-117">New Counter Set</span></span>
    -   <span data-ttu-id="3ca40-118">Ver atividade atual</span><span class="sxs-lookup"><span data-stu-id="3ca40-118">View Current Activity</span></span>
    -   <span data-ttu-id="3ca40-119">Exibir dados do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="3ca40-119">View Log File Data</span></span>
    -   <span data-ttu-id="3ca40-120">Adicionar</span><span class="sxs-lookup"><span data-stu-id="3ca40-120">Add</span></span>
    -   <span data-ttu-id="3ca40-121">Excluir</span><span class="sxs-lookup"><span data-stu-id="3ca40-121">Delete</span></span>
    -   <span data-ttu-id="3ca40-122">Colar lista de contadores</span><span class="sxs-lookup"><span data-stu-id="3ca40-122">Paste Counter List</span></span>
    -   <span data-ttu-id="3ca40-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ca40-123">Properties</span></span>

<span data-ttu-id="3ca40-124">Observe que essa propriedade afeta apenas a capacidade do usuário de modificar valores de propriedade por meio da interface do usuário; ela não impede que você modifique programaticamente os valores ou contadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3ca40-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca40-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ca40-125">Requirements</span></span>



| <span data-ttu-id="3ca40-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ca40-126">Requirement</span></span> | <span data-ttu-id="3ca40-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3ca40-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca40-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ca40-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca40-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ca40-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3ca40-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ca40-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca40-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ca40-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ca40-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca40-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ca40-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3ca40-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca40-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ca40-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca40-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3ca40-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





