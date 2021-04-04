---
title: Mensagem de TB_ISBUTTONENABLED (commctrl. h)
description: Determina se o botão especificado em uma barra de ferramentas está habilitado.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- Controles de TB_ISBUTTONENABLED de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824296"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="74241-104">TB de \_ mensagem ISBUTTONENABLED</span><span class="sxs-lookup"><span data-stu-id="74241-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="74241-105">Determina se o botão especificado em uma barra de ferramentas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="74241-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="74241-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74241-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74241-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74241-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="74241-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="74241-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74241-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74241-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="74241-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74241-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74241-111">Return value</span></span>

<span data-ttu-id="74241-112">Retornará zero se o botão estiver habilitado ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="74241-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="74241-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74241-113">Requirements</span></span>



| <span data-ttu-id="74241-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="74241-114">Requirement</span></span> | <span data-ttu-id="74241-115">Valor</span><span class="sxs-lookup"><span data-stu-id="74241-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74241-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74241-116">Minimum supported client</span></span><br/> | <span data-ttu-id="74241-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74241-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74241-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74241-118">Minimum supported server</span></span><br/> | <span data-ttu-id="74241-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74241-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74241-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74241-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="74241-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74241-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





