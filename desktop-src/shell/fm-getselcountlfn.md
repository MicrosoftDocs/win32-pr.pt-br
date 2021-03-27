---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar o número de arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela do diretório ou a janela de resultados da pesquisa). A contagem inclui arquivos que têm nomes de arquivo longos.
title: Mensagem de FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104989002"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="85e51-104">\_Mensagem GETSELCOUNTLFN de FM</span><span class="sxs-lookup"><span data-stu-id="85e51-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="85e51-105">Enviado por uma extensão do Gerenciador de arquivos para recuperar o número de arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela do diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="85e51-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="85e51-106">A contagem inclui arquivos que têm nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="85e51-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="85e51-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85e51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e51-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85e51-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="85e51-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="85e51-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="85e51-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85e51-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="85e51-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="85e51-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e51-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85e51-112">Return value</span></span>

<span data-ttu-id="85e51-113">Retorna o número de arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="85e51-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e51-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="85e51-114">Remarks</span></span>

<span data-ttu-id="85e51-115">Somente extensões que dão suporte a nomes de arquivo longos (por exemplo, extensões com reconhecimento de rede) devem usar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="85e51-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e51-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85e51-116">Requirements</span></span>



| <span data-ttu-id="85e51-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e51-117">Requirement</span></span> | <span data-ttu-id="85e51-118">Valor</span><span class="sxs-lookup"><span data-stu-id="85e51-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85e51-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85e51-119">Minimum supported client</span></span><br/> | <span data-ttu-id="85e51-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="85e51-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="85e51-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85e51-121">Minimum supported server</span></span><br/> | <span data-ttu-id="85e51-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="85e51-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85e51-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="85e51-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="85e51-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="85e51-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e51-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="85e51-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e51-126">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="85e51-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="85e51-127">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="85e51-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="85e51-128">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="85e51-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




