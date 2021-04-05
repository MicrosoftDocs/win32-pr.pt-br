---
title: Mensagem de TB_SETMAXTEXTROWS (commctrl. h)
description: Define o número máximo de linhas de texto exibidas em um botão da barra de ferramentas.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Controles de TB_SETMAXTEXTROWS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918167"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="e0c44-104">TB de \_ mensagem SETMAXTEXTROWS</span><span class="sxs-lookup"><span data-stu-id="e0c44-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="e0c44-105">Define o número máximo de linhas de texto exibidas em um botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e0c44-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0c44-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0c44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0c44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c44-108">Número máximo de linhas de texto que podem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="e0c44-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="e0c44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0c44-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e0c44-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e0c44-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c44-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0c44-111">Return value</span></span>

<span data-ttu-id="e0c44-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="e0c44-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c44-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0c44-113">Remarks</span></span>

<span data-ttu-id="e0c44-114">Para fazer com que o texto seja quebrado, você deve definir a largura máxima do botão enviando uma mensagem [**\_ SETBUTTONWIDTH TB**](tb-setbuttonwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="e0c44-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="e0c44-115">O texto é quebrado em uma quebra de palavra; quebras de linha (" \\ n") no texto são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="e0c44-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="e0c44-116">O texto nas \_ barras de ferramentas da lista de TBSTYLE sempre é mostrado em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="e0c44-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c44-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0c44-117">Requirements</span></span>



| <span data-ttu-id="e0c44-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0c44-118">Requirement</span></span> | <span data-ttu-id="e0c44-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e0c44-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c44-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0c44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c44-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0c44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0c44-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0c44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c44-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0c44-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0c44-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0c44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c44-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c44-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





