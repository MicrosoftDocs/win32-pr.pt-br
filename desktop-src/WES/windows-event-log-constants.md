---
title: Constantes do log de eventos do Windows (WinEvt. h)
description: O log de eventos do Windows define as seguintes constantes
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369593"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="bea53-103">Constantes do log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="bea53-103">Windows Event Log Constants</span></span>

<span data-ttu-id="bea53-104">O log de eventos do Windows define as seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="bea53-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="bea53-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_máscara do \_ tipo de variante de EVT \_**</span><span class="sxs-lookup"><span data-stu-id="bea53-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea53-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="bea53-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="bea53-107">Um bitmask que você usa para mascarar o bit da matriz do tipo Variant, de modo que você pode determinar o tipo de dados do valor da variante que a estrutura de [**\_ variante de EVT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) contém.</span><span class="sxs-lookup"><span data-stu-id="bea53-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bea53-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_matriz de \_ tipo de variante EVT \_**</span><span class="sxs-lookup"><span data-stu-id="bea53-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea53-109">128</span><span class="sxs-lookup"><span data-stu-id="bea53-109">128</span></span>
</dt> <dt>



<span data-ttu-id="bea53-110">O **tipo** membro da estrutura [**de \_ variante de EVT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) tem esse bit definido se a variante contiver um ponteiro para uma matriz de valores, em vez do próprio valor.</span><span class="sxs-lookup"><span data-stu-id="bea53-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bea53-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**\_acesso de leitura EVT \_**</span><span class="sxs-lookup"><span data-stu-id="bea53-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea53-112">0x1</span><span class="sxs-lookup"><span data-stu-id="bea53-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="bea53-113">Permissão de controle de acesso de leitura que permite que informações sejam lidas de um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="bea53-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bea53-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_acesso de gravação EVT \_**</span><span class="sxs-lookup"><span data-stu-id="bea53-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea53-115">0x2</span><span class="sxs-lookup"><span data-stu-id="bea53-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="bea53-116">Permissão de controle de acesso de gravação que permite que informações sejam gravadas em um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="bea53-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bea53-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT \_ limpar \_ acesso**</span><span class="sxs-lookup"><span data-stu-id="bea53-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea53-118">0x4</span><span class="sxs-lookup"><span data-stu-id="bea53-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="bea53-119">Desmarque a permissão controle de acesso que permite que todas as informações sejam limpas de um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="bea53-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bea53-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ todos os \_ acessos**</span><span class="sxs-lookup"><span data-stu-id="bea53-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea53-121">0x7</span><span class="sxs-lookup"><span data-stu-id="bea53-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="bea53-122">Permissão de controle de acesso All (leitura, gravação, limpeza e exclusão).</span><span class="sxs-lookup"><span data-stu-id="bea53-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bea53-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea53-123">Requirements</span></span>



| <span data-ttu-id="bea53-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea53-124">Requirement</span></span> | <span data-ttu-id="bea53-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bea53-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bea53-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bea53-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bea53-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bea53-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bea53-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bea53-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bea53-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bea53-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bea53-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bea53-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea53-131"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="bea53-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





