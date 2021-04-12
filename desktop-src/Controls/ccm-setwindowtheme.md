---
title: Mensagem de CCM_SETWINDOWTHEME (commctrl. h)
description: Define o estilo visual de um controle.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- Controles de CCM_SETWINDOWTHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455451"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="0d00a-104">CCM \_ SETWINDOWTHEME mensagem</span><span class="sxs-lookup"><span data-stu-id="0d00a-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="0d00a-105">Define o estilo visual de um controle.</span><span class="sxs-lookup"><span data-stu-id="0d00a-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d00a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d00a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d00a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d00a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d00a-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0d00a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d00a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d00a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d00a-110">Um ponteiro para uma cadeia de caracteres Unicode que contém o estilo visual de controle a ser definido.</span><span class="sxs-lookup"><span data-stu-id="0d00a-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d00a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d00a-111">Return value</span></span>

<span data-ttu-id="0d00a-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="0d00a-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d00a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d00a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0d00a-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="0d00a-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0d00a-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0d00a-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d00a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d00a-116">Requirements</span></span>



| <span data-ttu-id="0d00a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d00a-117">Requirement</span></span> | <span data-ttu-id="0d00a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0d00a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d00a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d00a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d00a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d00a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d00a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d00a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d00a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d00a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d00a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d00a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d00a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d00a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





