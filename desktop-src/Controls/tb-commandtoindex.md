---
title: Mensagem de TB_COMMANDTOINDEX (commctrl. h)
description: Recupera o índice de base zero para o botão associado ao identificador de comando especificado.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- Controles de TB_COMMANDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086531"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="c765b-104">TB de \_ mensagem COMMANDTOINDEX</span><span class="sxs-lookup"><span data-stu-id="c765b-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="c765b-105">Recupera o índice de base zero para o botão associado ao identificador de comando especificado.</span><span class="sxs-lookup"><span data-stu-id="c765b-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="c765b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c765b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c765b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c765b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c765b-108">Identificador de comando associado ao botão.</span><span class="sxs-lookup"><span data-stu-id="c765b-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="c765b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c765b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c765b-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c765b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c765b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c765b-111">Return value</span></span>

<span data-ttu-id="c765b-112">Retorna o índice de base zero para o botão ou-1 se o identificador de comando especificado for inválido.</span><span class="sxs-lookup"><span data-stu-id="c765b-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="c765b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c765b-113">Requirements</span></span>



| <span data-ttu-id="c765b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c765b-114">Requirement</span></span> | <span data-ttu-id="c765b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c765b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c765b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c765b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c765b-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c765b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c765b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c765b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c765b-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c765b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c765b-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c765b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c765b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c765b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





