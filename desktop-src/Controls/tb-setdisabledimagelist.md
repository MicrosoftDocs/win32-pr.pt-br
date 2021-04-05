---
title: Mensagem de TB_SETDISABLEDIMAGELIST (commctrl. h)
description: Define a lista de imagens que o controle Toolbar usará para exibir botões desabilitados.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- Controles de TB_SETDISABLEDIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009601"
---
# <a name="tb_setdisabledimagelist-message"></a><span data-ttu-id="aa942-104">TB de \_ mensagem SETDISABLEDIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="aa942-104">TB\_SETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="aa942-105">Define a lista de imagens que o controle Toolbar usará para exibir botões desabilitados.</span><span class="sxs-lookup"><span data-stu-id="aa942-105">Sets the image list that the toolbar control will use to display disabled buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa942-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa942-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa942-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aa942-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="aa942-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aa942-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa942-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa942-110">Identificador para a lista de imagens que será definida.</span><span class="sxs-lookup"><span data-stu-id="aa942-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa942-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa942-111">Return value</span></span>

<span data-ttu-id="aa942-112">Retorna o identificador para a lista de imagens usada anteriormente para exibir botões desabilitados ou **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="aa942-112">Returns the handle to the image list previously used to display disabled buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa942-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa942-113">Requirements</span></span>



| <span data-ttu-id="aa942-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa942-114">Requirement</span></span> | <span data-ttu-id="aa942-115">Valor</span><span class="sxs-lookup"><span data-stu-id="aa942-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa942-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa942-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa942-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa942-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa942-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa942-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa942-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa942-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa942-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa942-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa942-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa942-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





