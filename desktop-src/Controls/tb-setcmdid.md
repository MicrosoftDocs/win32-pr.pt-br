---
title: Mensagem de TB_SETCMDID (commctrl. h)
description: Define o identificador de comando de um botão da barra de ferramentas.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- Controles de TB_SETCMDID de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751303"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="7c3b4-104">TB de \_ mensagem SETCMDID</span><span class="sxs-lookup"><span data-stu-id="7c3b4-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="7c3b4-105">Define o identificador de comando de um botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="7c3b4-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c3b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c3b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c3b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3b4-108">Índice de base zero do botão cujo identificador de comando deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="7c3b4-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="7c3b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c3b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3b4-110">Identificador do comando.</span><span class="sxs-lookup"><span data-stu-id="7c3b4-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3b4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c3b4-111">Return value</span></span>

<span data-ttu-id="7c3b4-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7c3b4-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c3b4-113">Requirements</span></span>



| <span data-ttu-id="7c3b4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c3b4-114">Requirement</span></span> | <span data-ttu-id="7c3b4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7c3b4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3b4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3b4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3b4-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c3b4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c3b4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3b4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3b4-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c3b4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c3b4-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c3b4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c3b4-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c3b4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





