---
title: Mensagem de TB_GETBITMAP (commctrl. h)
description: Recupera o índice do bitmap associado a um botão em uma barra de ferramentas.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- Controles de TB_GETBITMAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919231"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="b02a9-104">+ TB de \_ mensagem de bitmap</span><span class="sxs-lookup"><span data-stu-id="b02a9-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="b02a9-105">Recupera o índice do bitmap associado a um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="b02a9-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b02a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b02a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b02a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b02a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b02a9-108">Identificador de comando do botão cujo índice de bitmap deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b02a9-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="b02a9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b02a9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b02a9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b02a9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b02a9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b02a9-111">Return value</span></span>

<span data-ttu-id="b02a9-112">Retorna o índice do bitmap se tiver êxito ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="b02a9-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b02a9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b02a9-113">Requirements</span></span>



| <span data-ttu-id="b02a9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02a9-114">Requirement</span></span> | <span data-ttu-id="b02a9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b02a9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b02a9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b02a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b02a9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b02a9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b02a9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b02a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b02a9-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b02a9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b02a9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b02a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02a9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b02a9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





