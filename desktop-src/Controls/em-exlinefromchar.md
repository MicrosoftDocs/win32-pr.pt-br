---
title: Mensagem de EM_EXLINEFROMCHAR (RichEdit. h)
description: Determina qual linha contém o caractere especificado em um controle de edição rico.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- Controles de EM_EXLINEFROMCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456060"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="be7d5-104">\_Mensagem em EXLINEFROMCHAR</span><span class="sxs-lookup"><span data-stu-id="be7d5-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="be7d5-105">Determina qual linha contém o caractere especificado em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="be7d5-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="be7d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be7d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be7d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be7d5-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="be7d5-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="be7d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be7d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be7d5-110">Índice de base zero do caractere.</span><span class="sxs-lookup"><span data-stu-id="be7d5-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be7d5-111">Return value</span></span>

<span data-ttu-id="be7d5-112">Essa mensagem retorna o índice de base zero da linha.</span><span class="sxs-lookup"><span data-stu-id="be7d5-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7d5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7d5-113">Requirements</span></span>



| <span data-ttu-id="be7d5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7d5-114">Requirement</span></span> | <span data-ttu-id="be7d5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="be7d5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be7d5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be7d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be7d5-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be7d5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be7d5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be7d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be7d5-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be7d5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be7d5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be7d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be7d5-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





