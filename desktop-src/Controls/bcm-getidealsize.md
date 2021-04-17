---
title: Mensagem de BCM_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho do botão que melhor se adapta a seu texto e imagem, se uma lista de imagens estiver presente. Você pode enviar essa mensagem explicitamente ou usar o botão \_ GetIdealSize macro.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Controles de BCM_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756240"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="56e82-105">\_Mensagem GETIDEALSIZE do BCM</span><span class="sxs-lookup"><span data-stu-id="56e82-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="56e82-106">Obtém o tamanho do botão que melhor se adapta a seu texto e imagem, se uma lista de imagens estiver presente.</span><span class="sxs-lookup"><span data-stu-id="56e82-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="56e82-107">Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span><span class="sxs-lookup"><span data-stu-id="56e82-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="56e82-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56e82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e82-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56e82-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56e82-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="56e82-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56e82-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56e82-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56e82-112">Um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que recebe o tamanho desejado do botão, incluindo a lista de texto e imagem, se presente.</span><span class="sxs-lookup"><span data-stu-id="56e82-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="56e82-113">O aplicativo de chamada é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="56e82-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="56e82-114">Defina os membros **CX** e **CY** como zero para que a altura e a largura ideais sejam retornadas na estrutura de **tamanho** .</span><span class="sxs-lookup"><span data-stu-id="56e82-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="56e82-115">Para especificar uma largura de botão, defina o membro **CX** para a largura de botão desejada.</span><span class="sxs-lookup"><span data-stu-id="56e82-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="56e82-116">O sistema calculará a altura ideal para essa largura e a retornará no membro **CY** .</span><span class="sxs-lookup"><span data-stu-id="56e82-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e82-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56e82-117">Return value</span></span>

<span data-ttu-id="56e82-118">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="56e82-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="56e82-119">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="56e82-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e82-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="56e82-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56e82-121">Se nenhuma largura de botão especial for desejada, você deverá definir ambos os membros de [**tamanho**](/previous-versions//dd145106(v=vs.85)) como zero para calcular e retornar a altura e a largura ideais.</span><span class="sxs-lookup"><span data-stu-id="56e82-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="56e82-122">Se o valor do membro **CX** for maior que zero, esse valor será considerado a largura do botão desejado e a altura ideal para essa largura será calculada e retornada no membro **CY** .</span><span class="sxs-lookup"><span data-stu-id="56e82-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="56e82-123">Essa mensagem é mais aplicável a supressãos.</span><span class="sxs-lookup"><span data-stu-id="56e82-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="56e82-124">Quando enviado a um botão de pressão, a mensagem recupera o retângulo delimitador necessário para exibir o texto do Button.</span><span class="sxs-lookup"><span data-stu-id="56e82-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="56e82-125">Além disso, se o botão de pressão tiver uma lista de imagens, o retângulo delimitador também será dimensionado para incluir a imagem do botão.</span><span class="sxs-lookup"><span data-stu-id="56e82-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="56e82-126">Quando enviado a um botão de qualquer outro tipo, o tamanho do retângulo da janela do controle é recuperado.</span><span class="sxs-lookup"><span data-stu-id="56e82-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="56e82-127">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="56e82-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="56e82-128">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="56e82-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56e82-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56e82-129">Requirements</span></span>



| <span data-ttu-id="56e82-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="56e82-130">Requirement</span></span> | <span data-ttu-id="56e82-131">Valor</span><span class="sxs-lookup"><span data-stu-id="56e82-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56e82-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56e82-132">Minimum supported client</span></span><br/> | <span data-ttu-id="56e82-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56e82-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56e82-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56e82-134">Minimum supported server</span></span><br/> | <span data-ttu-id="56e82-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56e82-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56e82-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56e82-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="56e82-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e82-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

