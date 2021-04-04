---
title: Mensagem de LVM_SETOUTLINECOLOR (commctrl. h)
description: Define a cor da borda de um controle de exibição de lista se o \_ estilo de \_ janela estendida LVS ex BORDERSELECT for definido.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Controles de LVM_SETOUTLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824167"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="c65c6-104">\_Mensagem SETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="c65c6-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="c65c6-105">Define a cor da borda de um controle de exibição de lista se o estilo de janela estendida [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) for definido.</span><span class="sxs-lookup"><span data-stu-id="c65c6-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="c65c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c65c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c65c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c65c6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c65c6-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c65c6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c65c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c65c6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c65c6-110">Estrutura **COLORREF** que especifica a cor para definir a borda.</span><span class="sxs-lookup"><span data-stu-id="c65c6-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c65c6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c65c6-111">Return value</span></span>

<span data-ttu-id="c65c6-112">Retorna a estrutura **COLORREF** que contém a cor da estrutura de tópicos.</span><span class="sxs-lookup"><span data-stu-id="c65c6-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="c65c6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c65c6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c65c6-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="c65c6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c65c6-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c65c6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c65c6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c65c6-116">Requirements</span></span>



| <span data-ttu-id="c65c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c65c6-117">Requirement</span></span> | <span data-ttu-id="c65c6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c65c6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c65c6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c65c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c65c6-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c65c6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c65c6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c65c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c65c6-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c65c6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c65c6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c65c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c65c6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c65c6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





