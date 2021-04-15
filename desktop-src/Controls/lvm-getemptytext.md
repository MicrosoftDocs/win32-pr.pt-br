---
title: Mensagem de LVM_GETEMPTYTEXT (commctrl. h)
description: Obtém o texto destinado à exibição quando o controle de exibição de lista aparece vazio. Envie essa mensagem explicitamente ou usando a \_ macro GetEmptyText do ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Controles de LVM_GETEMPTYTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454630"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="61a3c-105">\_Mensagem GETEMPTYTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="61a3c-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="61a3c-106">Obtém o texto destinado à exibição quando o controle de exibição de lista aparece vazio.</span><span class="sxs-lookup"><span data-stu-id="61a3c-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="61a3c-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetEmptyText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .</span><span class="sxs-lookup"><span data-stu-id="61a3c-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61a3c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61a3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a3c-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61a3c-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a3c-110">O tamanho do buffer apontado por *lParam*, incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="61a3c-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="61a3c-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="61a3c-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61a3c-112">Um ponteiro para um buffer Unicode com terminação nula de tamanho especificado por *wParam* para receber o texto.</span><span class="sxs-lookup"><span data-stu-id="61a3c-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="61a3c-113">O chamador é responsável por alocar o buffer.</span><span class="sxs-lookup"><span data-stu-id="61a3c-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a3c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61a3c-114">Return value</span></span>

<span data-ttu-id="61a3c-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="61a3c-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a3c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a3c-116">Requirements</span></span>



| <span data-ttu-id="61a3c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a3c-117">Requirement</span></span> | <span data-ttu-id="61a3c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="61a3c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61a3c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61a3c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="61a3c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61a3c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61a3c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61a3c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="61a3c-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61a3c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61a3c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61a3c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a3c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a3c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





