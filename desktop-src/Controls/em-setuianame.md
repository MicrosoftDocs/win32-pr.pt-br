---
title: Mensagem de EM_SETUIANAME (RichEdit. h)
description: Define o nome de um controle de edição rico para a automação da interface do usuário (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Controles de EM_SETUIANAME de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918615"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="6dd0d-104">\_Mensagem em SETUIANAME</span><span class="sxs-lookup"><span data-stu-id="6dd0d-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="6dd0d-105">Define o nome de um controle de edição rico para a automação da interface do usuário (UIA).</span><span class="sxs-lookup"><span data-stu-id="6dd0d-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="6dd0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dd0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd0d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6dd0d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dd0d-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6dd0d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6dd0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6dd0d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dd0d-110">Um ponteiro para a cadeia de caracteres de nome terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6dd0d-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd0d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dd0d-111">Return value</span></span>

<span data-ttu-id="6dd0d-112">TRUE se o nome de UIA for definido com êxito; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="6dd0d-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd0d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dd0d-113">Requirements</span></span>



| <span data-ttu-id="6dd0d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd0d-114">Requirement</span></span> | <span data-ttu-id="6dd0d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6dd0d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd0d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dd0d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd0d-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6dd0d-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6dd0d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dd0d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd0d-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6dd0d-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6dd0d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dd0d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dd0d-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dd0d-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





