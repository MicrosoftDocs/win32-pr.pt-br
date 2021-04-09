---
title: Mensagem de RB_SETWINDOWTHEME (commctrl. h)
description: Define o estilo visual de um controle rebar.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- Controles de RB_SETWINDOWTHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085922"
---
# <a name="rb_setwindowtheme-message"></a><span data-ttu-id="2c03a-104">\_Mensagem SETWINDOWTHEME RB</span><span class="sxs-lookup"><span data-stu-id="2c03a-104">RB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="2c03a-105">Define o estilo visual de um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="2c03a-105">Sets the visual style of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c03a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c03a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c03a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c03a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2c03a-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2c03a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2c03a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c03a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c03a-110">Ponteiro para uma cadeia de caracteres Unicode que contém o estilo visual rebar a ser definido.</span><span class="sxs-lookup"><span data-stu-id="2c03a-110">Pointer to a Unicode string that contains the rebar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c03a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c03a-111">Return value</span></span>

<span data-ttu-id="2c03a-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="2c03a-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c03a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c03a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c03a-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="2c03a-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2c03a-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2c03a-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c03a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c03a-116">Requirements</span></span>



| <span data-ttu-id="2c03a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c03a-117">Requirement</span></span> | <span data-ttu-id="2c03a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2c03a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c03a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c03a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c03a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c03a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c03a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c03a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c03a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c03a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c03a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c03a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c03a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c03a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





