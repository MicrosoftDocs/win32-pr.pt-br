---
title: Mensagem de TB_CHANGEBITMAP (commctrl. h)
description: Altera o bitmap de um botão em uma barra de ferramentas.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Controles de TB_CHANGEBITMAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824849"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="220f5-104">TB de \_ mensagem CHANGEBITMAP</span><span class="sxs-lookup"><span data-stu-id="220f5-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="220f5-105">Altera o bitmap de um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="220f5-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="220f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="220f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="220f5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="220f5-108">Identificador de comando do botão que deve receber um novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="220f5-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="220f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="220f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="220f5-110">Índice de base zero de uma imagem na lista de imagens da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="220f5-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="220f5-111">O sistema exibe a imagem especificada no botão.</span><span class="sxs-lookup"><span data-stu-id="220f5-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="220f5-112">Defina esse parâmetro como I \_ IMAGECALLBACK e a barra de ferramentas enviará a notificação [**tbn \_ GETDISPINFO**](tbn-getdispinfo.md) para recuperar o índice de imagem quando necessário.</span><span class="sxs-lookup"><span data-stu-id="220f5-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="220f5-113">[Versão 5,81](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="220f5-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="220f5-114">Defina esse parâmetro como I \_ IMAGENONE para indicar que o botão não tem uma imagem.</span><span class="sxs-lookup"><span data-stu-id="220f5-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="220f5-115">O layout do botão não incluirá nenhum espaço para um bitmap, somente texto.</span><span class="sxs-lookup"><span data-stu-id="220f5-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220f5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="220f5-116">Return value</span></span>

<span data-ttu-id="220f5-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="220f5-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="220f5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="220f5-118">Requirements</span></span>



| <span data-ttu-id="220f5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="220f5-119">Requirement</span></span> | <span data-ttu-id="220f5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="220f5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="220f5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="220f5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="220f5-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="220f5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="220f5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="220f5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="220f5-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="220f5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="220f5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="220f5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="220f5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="220f5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





