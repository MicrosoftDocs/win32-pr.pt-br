---
description: Enviado por uma extensão do Gerenciador de arquivos para fazer com que o Gerenciador de arquivos repinte sua janela ativa ou todas as suas janelas.
title: Mensagem de FM_REFRESH_WINDOWS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842347"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="eed68-103">Mensagem de atualização de FM do \_ \_ Windows</span><span class="sxs-lookup"><span data-stu-id="eed68-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="eed68-104">Enviado por uma extensão do Gerenciador de arquivos para fazer com que o Gerenciador de arquivos repinte sua janela ativa ou todas as suas janelas.</span><span class="sxs-lookup"><span data-stu-id="eed68-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="eed68-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eed68-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed68-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="eed68-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="eed68-107">Um valor que indica se o Gerenciador de arquivos redesenha sua janela ativa ou todas as suas janelas.</span><span class="sxs-lookup"><span data-stu-id="eed68-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="eed68-108">Se esse parâmetro for **true**, o Gerenciador de arquivos repintará todas as suas janelas.</span><span class="sxs-lookup"><span data-stu-id="eed68-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="eed68-109">Caso contrário, o Gerenciador de arquivos repintará apenas sua janela ativa.</span><span class="sxs-lookup"><span data-stu-id="eed68-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="eed68-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eed68-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eed68-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="eed68-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed68-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eed68-112">Return value</span></span>

<span data-ttu-id="eed68-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="eed68-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed68-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eed68-114">Remarks</span></span>

<span data-ttu-id="eed68-115">As alterações do sistema de arquivos causadas por uma extensão são detectadas automaticamente pelo Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="eed68-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="eed68-116">Uma extensão deve usar essa mensagem somente em situações em que as conexões de unidade são feitas ou canceladas.</span><span class="sxs-lookup"><span data-stu-id="eed68-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed68-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed68-117">Requirements</span></span>



| <span data-ttu-id="eed68-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed68-118">Requirement</span></span> | <span data-ttu-id="eed68-119">Valor</span><span class="sxs-lookup"><span data-stu-id="eed68-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eed68-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eed68-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eed68-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eed68-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="eed68-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eed68-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eed68-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eed68-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eed68-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eed68-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eed68-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed68-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed68-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="eed68-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed68-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="eed68-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




