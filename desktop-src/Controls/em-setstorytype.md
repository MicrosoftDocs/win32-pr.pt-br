---
title: Mensagem de EM_SETSTORYTYPE (RichEdit. h)
description: Define o tipo de história.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Controles de EM_SETSTORYTYPE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824303"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="4be5b-104">\_Mensagem em SEThistóriatype</span><span class="sxs-lookup"><span data-stu-id="4be5b-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="4be5b-105">Define o tipo de história.</span><span class="sxs-lookup"><span data-stu-id="4be5b-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="4be5b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4be5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be5b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4be5b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4be5b-108">O índice da história.</span><span class="sxs-lookup"><span data-stu-id="4be5b-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="4be5b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4be5b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4be5b-110">O novo tipo de história.</span><span class="sxs-lookup"><span data-stu-id="4be5b-110">The new story type.</span></span> <span data-ttu-id="4be5b-111">Para obter uma lista de tipos de história, consulte em [**\_ gethistóriatype**](em-getstorytype.md).</span><span class="sxs-lookup"><span data-stu-id="4be5b-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be5b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4be5b-112">Return value</span></span>

<span data-ttu-id="4be5b-113">O tipo de história que foi definido.</span><span class="sxs-lookup"><span data-stu-id="4be5b-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be5b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be5b-114">Requirements</span></span>



| <span data-ttu-id="4be5b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be5b-115">Requirement</span></span> | <span data-ttu-id="4be5b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4be5b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4be5b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4be5b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4be5b-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4be5b-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4be5b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4be5b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4be5b-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4be5b-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4be5b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4be5b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be5b-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be5b-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





