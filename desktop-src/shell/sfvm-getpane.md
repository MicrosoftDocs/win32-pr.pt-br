---
description: SFVM \_ GetPane pode ser alterado ou indisponível.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Mensagem de SFVM_GETPANE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922067"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="dd1ce-103">Mensagem do SFVM \_ GETpane</span><span class="sxs-lookup"><span data-stu-id="dd1ce-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="dd1ce-104">\[**SFVM \_ GetPane** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd1ce-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="dd1ce-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="dd1ce-106">Permite que o objeto de retorno de chamada forneça o painel barra de status para exibir as informações da zona da Internet.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="dd1ce-107">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="dd1ce-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="dd1ce-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd1ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1ce-109">*painel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd1ce-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1ce-110">ID do painel solicitado.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-110">ID of the requested pane.</span></span> <span data-ttu-id="dd1ce-111">Normalmente, essa é \_ a zona do painel, mas pode ser qualquer um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="dd1ce-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PAINEL \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-113">Nenhum painel.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="dd1ce-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**zona do painel \_**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-115">O painel zona da Internet.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="dd1ce-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PAINEL \_ offline**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-117">O painel offline.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="dd1ce-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**impressora do painel \_**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-119">O painel de indicação de impressão.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="dd1ce-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PAINEL \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-121">O painel SSL.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="dd1ce-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**navegação do painel \_**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-123">O painel de navegação.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="dd1ce-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**progresso do painel \_**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-125">O painel de barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="dd1ce-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**privacidade do painel \_**</span><span class="sxs-lookup"><span data-stu-id="dd1ce-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="dd1ce-127">O painel de indicadores de privacidade.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dd1ce-128">*painel* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dd1ce-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1ce-129">Ponteiro para um **DWORD** que contém o número do painel.</span><span class="sxs-lookup"><span data-stu-id="dd1ce-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd1ce-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd1ce-130">Requirements</span></span>



| <span data-ttu-id="dd1ce-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd1ce-131">Requirement</span></span> | <span data-ttu-id="dd1ce-132">Valor</span><span class="sxs-lookup"><span data-stu-id="dd1ce-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1ce-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd1ce-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1ce-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd1ce-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dd1ce-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd1ce-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1ce-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd1ce-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dd1ce-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dd1ce-137">End of client support</span></span><br/>    | <span data-ttu-id="dd1ce-138">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="dd1ce-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="dd1ce-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="dd1ce-139">End of server support</span></span><br/>    | <span data-ttu-id="dd1ce-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd1ce-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="dd1ce-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd1ce-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd1ce-142"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1ce-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
