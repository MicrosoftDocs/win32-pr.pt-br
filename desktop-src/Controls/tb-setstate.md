---
title: Mensagem de TB_SETSTATE (commctrl. h)
description: Define o estado do botão especificado em uma barra de ferramentas.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- Controles de TB_SETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086525"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="71e3d-104">Restate de TB de \_ mensagem</span><span class="sxs-lookup"><span data-stu-id="71e3d-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="71e3d-105">Define o estado do botão especificado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="71e3d-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="71e3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71e3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71e3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e3d-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="71e3d-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="71e3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71e3d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e3d-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é uma combinação de valores listados em [Estados de botão da barra de ferramentas](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="71e3d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="71e3d-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="71e3d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e3d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71e3d-112">Return value</span></span>

<span data-ttu-id="71e3d-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="71e3d-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e3d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71e3d-114">Requirements</span></span>



| <span data-ttu-id="71e3d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e3d-115">Requirement</span></span> | <span data-ttu-id="71e3d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="71e3d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71e3d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71e3d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71e3d-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71e3d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71e3d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71e3d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71e3d-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71e3d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71e3d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71e3d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e3d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e3d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

