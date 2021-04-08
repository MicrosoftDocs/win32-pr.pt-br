---
title: Mensagem de TB_GETBITMAPFLAGS (commctrl. h)
description: Recupera os sinalizadores que descrevem o tipo de bitmap a ser usado.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Controles de TB_GETBITMAPFLAGS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086530"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="35292-104">TB de \_ mensagem GETBITMAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="35292-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="35292-105">Recupera os sinalizadores que descrevem o tipo de bitmap a ser usado.</span><span class="sxs-lookup"><span data-stu-id="35292-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="35292-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35292-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35292-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="35292-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="35292-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="35292-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35292-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="35292-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="35292-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35292-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35292-111">Return value</span></span>

<span data-ttu-id="35292-112">Retorna um valor **DWORD** que descreve o tipo de bitmap que deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="35292-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="35292-113">Se esse valor de retorno tiver o \_ sinalizador grande TBBF, os aplicativos deverão usar bitmaps grandes (24 x 24); caso contrário, os aplicativos deverão usar bitmaps pequenos (16 x 16).</span><span class="sxs-lookup"><span data-stu-id="35292-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="35292-114">Todos os outros bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="35292-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="35292-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="35292-115">Remarks</span></span>

<span data-ttu-id="35292-116">O valor retornado por **TB \_ GETBITMAPFLAGS** é apenas consultor.</span><span class="sxs-lookup"><span data-stu-id="35292-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="35292-117">O controle Toolbar recomenda bitmaps grandes ou pequenos com base no fato de o usuário ter escolhido fontes grandes ou pequenas.</span><span class="sxs-lookup"><span data-stu-id="35292-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="35292-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35292-118">Requirements</span></span>



| <span data-ttu-id="35292-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="35292-119">Requirement</span></span> | <span data-ttu-id="35292-120">Valor</span><span class="sxs-lookup"><span data-stu-id="35292-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35292-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35292-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35292-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35292-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35292-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35292-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35292-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35292-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35292-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35292-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="35292-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35292-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





