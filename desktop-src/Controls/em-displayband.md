---
title: Mensagem de EM_DISPLAYBAND (RichEdit. h)
description: Exibe uma parte do conteúdo de um controle rich edit, conforme formatado anteriormente para um dispositivo usando a mensagem em \_ FormatRange.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Controles de EM_DISPLAYBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918708"
---
# <a name="em_displayband-message"></a><span data-ttu-id="e6428-104">\_Mensagem em DISPLAYBAND</span><span class="sxs-lookup"><span data-stu-id="e6428-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="e6428-105">Exibe uma parte do conteúdo de um controle rich edit, conforme formatado anteriormente para um dispositivo usando a mensagem [**em \_ FORMATRANGE**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="e6428-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6428-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6428-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6428-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6428-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e6428-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e6428-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6428-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6428-110">Uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica a área de exibição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6428-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6428-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6428-111">Return value</span></span>

<span data-ttu-id="e6428-112">Se a operação for concluída com sucesso, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="e6428-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="e6428-113">Se a operação falhar, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="e6428-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6428-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6428-114">Remarks</span></span>

<span data-ttu-id="e6428-115">Os objetos de texto e Component Object Model (COM) são recortados pelo retângulo.</span><span class="sxs-lookup"><span data-stu-id="e6428-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="e6428-116">O aplicativo não precisa definir a região de recorte.</span><span class="sxs-lookup"><span data-stu-id="e6428-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="e6428-117">A faixa é o processo pelo qual uma única página de saída é gerada usando um ou mais retângulos ou faixas separadas.</span><span class="sxs-lookup"><span data-stu-id="e6428-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="e6428-118">Quando todas as faixas são colocadas na página, uma imagem completa resulta.</span><span class="sxs-lookup"><span data-stu-id="e6428-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="e6428-119">Essa abordagem é geralmente usada por impressoras rasterizadas que não têm memória suficiente ou capacidade de fazer a imagem de uma página inteira ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e6428-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="e6428-120">Os dispositivos de faixa incluem a maioria das impressoras de matriz de pontos, bem como algumas impressoras a laser.</span><span class="sxs-lookup"><span data-stu-id="e6428-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6428-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6428-121">Requirements</span></span>



| <span data-ttu-id="e6428-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6428-122">Requirement</span></span> | <span data-ttu-id="e6428-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e6428-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6428-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6428-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6428-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6428-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6428-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6428-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6428-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6428-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6428-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6428-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6428-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6428-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6428-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6428-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6428-131">Imprimindo controles de edição avançada</span><span class="sxs-lookup"><span data-stu-id="e6428-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

