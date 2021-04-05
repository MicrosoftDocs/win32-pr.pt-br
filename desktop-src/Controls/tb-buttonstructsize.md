---
title: Mensagem de TB_BUTTONSTRUCTSIZE (commctrl. h)
description: Especifica o tamanho da estrutura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Controles de TB_BUTTONSTRUCTSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009775"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="39eba-104">TB de \_ mensagem BUTTONSTRUCTSIZE</span><span class="sxs-lookup"><span data-stu-id="39eba-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="39eba-105">Especifica o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="39eba-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="39eba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39eba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39eba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39eba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39eba-108">Tamanho, em bytes, da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="39eba-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="39eba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39eba-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="39eba-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="39eba-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39eba-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39eba-111">Return value</span></span>

<span data-ttu-id="39eba-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="39eba-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39eba-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="39eba-113">Remarks</span></span>

<span data-ttu-id="39eba-114">O sistema usa o tamanho para determinar qual versão da DLL (biblioteca de vínculo dinâmico) de controle comum está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="39eba-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="39eba-115">Se um aplicativo usar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar a barra de ferramentas, o aplicativo deverá enviar essa mensagem para a barra de ferramentas antes de enviar a mensagem de \* [**TB \_ AddBitmap**](tb-addbitmap.md) ou [**TB \_**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="39eba-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="39eba-116">A função [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envia automaticamente **TB \_ BUTTONSTRUCTSIZE** e o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) é um parâmetro da função.</span><span class="sxs-lookup"><span data-stu-id="39eba-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="39eba-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39eba-117">Requirements</span></span>



| <span data-ttu-id="39eba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="39eba-118">Requirement</span></span> | <span data-ttu-id="39eba-119">Valor</span><span class="sxs-lookup"><span data-stu-id="39eba-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39eba-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39eba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39eba-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39eba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39eba-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39eba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39eba-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39eba-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39eba-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39eba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="39eba-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39eba-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

