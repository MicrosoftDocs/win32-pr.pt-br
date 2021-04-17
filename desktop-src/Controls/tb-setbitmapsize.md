---
title: Mensagem de TB_SETBITMAPSIZE (commctrl. h)
description: Define o tamanho das imagens de bitmap a serem adicionadas a uma barra de ferramentas.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Controles de TB_SETBITMAPSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454620"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="b6db3-104">TB de \_ mensagem SETBITMAPSIZE</span><span class="sxs-lookup"><span data-stu-id="b6db3-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="b6db3-105">Define o tamanho das imagens de bitmap a serem adicionadas a uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="b6db3-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6db3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6db3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6db3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6db3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6db3-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b6db3-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6db3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6db3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6db3-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura, em pixels, das imagens de bitmap.</span><span class="sxs-lookup"><span data-stu-id="b6db3-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="b6db3-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a altura, em pixels, das imagens de bitmap.</span><span class="sxs-lookup"><span data-stu-id="b6db3-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6db3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6db3-112">Return value</span></span>

<span data-ttu-id="b6db3-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b6db3-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6db3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6db3-114">Remarks</span></span>

<span data-ttu-id="b6db3-115">O tamanho pode ser definido somente antes de adicionar qualquer bitmap à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="b6db3-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="b6db3-116">Se um aplicativo não definir explicitamente o tamanho do bitmap, o tamanho padrão será 16 por 15 pixels.</span><span class="sxs-lookup"><span data-stu-id="b6db3-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6db3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6db3-117">Requirements</span></span>



| <span data-ttu-id="b6db3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6db3-118">Requirement</span></span> | <span data-ttu-id="b6db3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b6db3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6db3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6db3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6db3-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6db3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6db3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6db3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6db3-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6db3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6db3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6db3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6db3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6db3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

