---
title: Mensagem de LVM_GETOUTLINECOLOR (commctrl. h)
description: Recupera a cor da borda de um controle de exibição de lista se o \_ estilo de \_ janela estendida LVS ex BORDERSELECT for definido.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Controles de LVM_GETOUTLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824669"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="fa1fb-104">\_Mensagem GETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="fa1fb-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="fa1fb-105">Recupera a cor da borda de um controle de exibição de lista se o estilo de janela estendida [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) for definido.</span><span class="sxs-lookup"><span data-stu-id="fa1fb-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa1fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa1fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa1fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa1fb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa1fb-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fa1fb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fa1fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa1fb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa1fb-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fa1fb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa1fb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa1fb-111">Return value</span></span>

<span data-ttu-id="fa1fb-112">Retorna uma estrutura **COLORREF** que contém a cor da borda de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="fa1fb-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa1fb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa1fb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa1fb-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="fa1fb-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fa1fb-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fa1fb-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa1fb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa1fb-116">Requirements</span></span>



| <span data-ttu-id="fa1fb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa1fb-117">Requirement</span></span> | <span data-ttu-id="fa1fb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fa1fb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1fb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa1fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fa1fb-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa1fb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa1fb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa1fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fa1fb-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa1fb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa1fb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa1fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa1fb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa1fb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





