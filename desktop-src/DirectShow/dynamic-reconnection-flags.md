---
description: Os sinalizadores a seguir especificam o nível de reconexão dinâmica a ser usado durante a renderização.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Sinalizadores de reconexão dinâmica (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780636"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="e7465-103">Sinalizadores de reconexão dinâmica</span><span class="sxs-lookup"><span data-stu-id="e7465-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="e7465-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e7465-104">\[Deprecated.</span></span> <span data-ttu-id="e7465-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7465-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="e7465-106">Os sinalizadores a seguir especificam o nível de reconexão dinâmica a ser usado durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="e7465-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="e7465-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e7465-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="e7465-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7465-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="e7465-109"><dt>**CONNECTF \_ DINÂMICO \_ nenhum**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="e7465-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="e7465-110">Nenhuma reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="e7465-110">No dynamic reconnection.</span></span> <span data-ttu-id="e7465-111">Carregar tudo antes de renderizar o projeto.</span><span class="sxs-lookup"><span data-stu-id="e7465-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="e7465-112"><dt>**CONNECTF \_ \_Origens dinâmicas**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e7465-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e7465-113">Carregue as fontes somente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e7465-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="e7465-114"><dt>**CONNECTF \_ \_Efeitos dinâmicos**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e7465-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="e7465-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e7465-115">Reserved.</span></span> <span data-ttu-id="e7465-116">Não use.</span><span class="sxs-lookup"><span data-stu-id="e7465-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="e7465-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7465-117">Requirements</span></span>



| <span data-ttu-id="e7465-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7465-118">Requirement</span></span> | <span data-ttu-id="e7465-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e7465-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7465-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7465-120">Header</span></span><br/> | <dl> <span data-ttu-id="e7465-121"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7465-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7465-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7465-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7465-123">**IRenderEngine::SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="e7465-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




