---
title: Mensagem de CCM_GETVERSION (commctrl. h)
description: Obtém o número de versão de um conjunto de controle pela mensagem CCM \_ SetVersion mais recente.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Controles de CCM_GETVERSION de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085833"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="b7353-104">\_Mensagem CCM GETversion</span><span class="sxs-lookup"><span data-stu-id="b7353-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="b7353-105">Obtém o número de versão de um conjunto de controle pela mensagem [**CCM \_ SetVersion**](ccm-setversion.md) mais recente.</span><span class="sxs-lookup"><span data-stu-id="b7353-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7353-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7353-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7353-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7353-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b7353-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b7353-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b7353-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7353-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b7353-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b7353-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7353-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7353-111">Return value</span></span>

<span data-ttu-id="b7353-112">Retorna o número de versão definido pela mensagem CCM mais recente da [**\_ objectVersion**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b7353-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="b7353-113">Se nenhuma mensagem desse tipo tiver sido enviada, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b7353-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7353-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7353-114">Remarks</span></span>

<span data-ttu-id="b7353-115">Essa mensagem não retorna a versão da DLL.</span><span class="sxs-lookup"><span data-stu-id="b7353-115">This message does not return the DLL version.</span></span> <span data-ttu-id="b7353-116">Confira [versões do Shell](common-control-versions.md) para obter uma discussão de como usar o [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar a versão atual da dll.</span><span class="sxs-lookup"><span data-stu-id="b7353-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="b7353-117">O número de versão é definido com base em controle por controle e pode não ser o mesmo para todos os controles.</span><span class="sxs-lookup"><span data-stu-id="b7353-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7353-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7353-118">Requirements</span></span>



| <span data-ttu-id="b7353-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7353-119">Requirement</span></span> | <span data-ttu-id="b7353-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7353-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7353-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7353-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7353-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7353-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7353-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7353-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7353-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7353-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7353-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7353-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7353-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7353-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

