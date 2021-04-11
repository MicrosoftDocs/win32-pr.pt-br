---
title: Valores de WTNCA (uxtheme. h)
description: Especifica os sinalizadores que modificam os atributos de estilo visual da janela. Use uma combinação de bits ou bit-a-bit dos valores a seguir.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086309"
---
# <a name="wtnca-values"></a><span data-ttu-id="ae048-104">Valores de WTNCA</span><span class="sxs-lookup"><span data-stu-id="ae048-104">WTNCA Values</span></span>

<span data-ttu-id="ae048-105">Especifica os sinalizadores que modificam os atributos de estilo visual da janela.</span><span class="sxs-lookup"><span data-stu-id="ae048-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="ae048-106">Use uma combinação de bits ou bit-a-bit dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae048-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="ae048-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="ae048-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="ae048-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae048-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="ae048-109"><dt>**WTNCA \_ NODRAWCAPTION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ae048-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ae048-110">Impede que a legenda da janela seja desenhada.</span><span class="sxs-lookup"><span data-stu-id="ae048-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="ae048-111"><dt>**WTNCA \_ NODRAWICON**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ae048-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="ae048-112">Impede que o ícone do sistema seja desenhado.</span><span class="sxs-lookup"><span data-stu-id="ae048-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="ae048-113"><dt>**WTNCA \_ NOSYSMENU**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ae048-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="ae048-114">Impede que o menu de ícone do sistema apareça.</span><span class="sxs-lookup"><span data-stu-id="ae048-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="ae048-115"><dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="ae048-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="ae048-116">Impede o espelhamento do ponto de interrogação, mesmo no layout da direita para a esquerda (RTL).</span><span class="sxs-lookup"><span data-stu-id="ae048-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="ae048-117"><dt>**WTNCA \_ VALIDBITS**</dt></span><span class="sxs-lookup"><span data-stu-id="ae048-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="ae048-118">Uma máscara que contém todos os bits válidos.</span><span class="sxs-lookup"><span data-stu-id="ae048-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="ae048-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae048-119">Requirements</span></span>



| <span data-ttu-id="ae048-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae048-120">Requirement</span></span> | <span data-ttu-id="ae048-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ae048-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ae048-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae048-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae048-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae048-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ae048-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae048-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae048-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae048-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ae048-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae048-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae048-127"><dt>Uxtheme. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae048-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae048-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae048-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae048-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ae048-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ae048-130">**opções de WTA \_**</span><span class="sxs-lookup"><span data-stu-id="ae048-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="ae048-131">**SetWindowThemeNonClientAttributes**</span><span class="sxs-lookup"><span data-stu-id="ae048-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





