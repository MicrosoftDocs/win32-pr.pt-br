---
title: Mensagem de CCM_DPISCALE (commctrl. h)
description: Habilita o dimensionamento automático de pontos por polegada (DPI) em controles de Tree-View, controles de List-View, controles de ComboBoxEx, controles de cabeçalho, botões, controles de barra de ferramentas, controles de animação e listas de imagens.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Controles de CCM_DPISCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085835"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="4d9e6-104">CCM \_ DPISCALE mensagem</span><span class="sxs-lookup"><span data-stu-id="4d9e6-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="4d9e6-105">Habilita o dimensionamento automático de pontos por polegada (DPI) em [controles de exibição de árvore](tree-view-controls.md), controles de exibição de [lista](list-view-control-reference.md), [controles de ComboBoxEx](comboboxex-controls.md), controles de [cabeçalho](header-controls.md), [botões](buttons.md), controles de [barra de ferramentas](toolbar-controls-overview.md), [controles de animação](animation-control-overview.md)e [listas de imagens](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="4d9e6-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="4d9e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d9e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d9e6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d9e6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d9e6-108">Defina como **true**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4d9e6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d9e6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d9e6-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d9e6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d9e6-111">Return value</span></span>

<span data-ttu-id="4d9e6-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d9e6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d9e6-113">Remarks</span></span>

<span data-ttu-id="4d9e6-114">O início rápido e a [barra de tarefas](/windows/desktop/shell/taskbar) não devem especificar um dimensionamento de DPI, pois as imagens já estão dimensionadas.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="4d9e6-115">Qualquer controle que usa uma lista de imagens criada com a métrica SmallIcon não deve dimensionar seus ícones.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="4d9e6-116">Para usar essa API, você deve fornecer um manifesto que especifique Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4d9e6-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4d9e6-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d9e6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d9e6-118">Requirements</span></span>



| <span data-ttu-id="4d9e6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d9e6-119">Requirement</span></span> | <span data-ttu-id="4d9e6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4d9e6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9e6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d9e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4d9e6-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d9e6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d9e6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d9e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4d9e6-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d9e6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d9e6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d9e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d9e6-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

