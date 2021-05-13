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
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841337"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="e158b-104">\_Mensagem GETSELCOUNTLFN de FM</span><span class="sxs-lookup"><span data-stu-id="e158b-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="e158b-105">Enviado por uma extensão do Gerenciador de arquivos para recuperar o número de arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela do diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="e158b-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="e158b-106">A contagem inclui arquivos que têm nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="e158b-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="e158b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e158b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e158b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e158b-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e158b-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e158b-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e158b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e158b-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e158b-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e158b-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e158b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e158b-112">Return value</span></span>

<span data-ttu-id="e158b-113">Retorna o número de arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="e158b-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="e158b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e158b-114">Remarks</span></span>

<span data-ttu-id="e158b-115">Somente extensões que dão suporte a nomes de arquivo longos (por exemplo, extensões com reconhecimento de rede) devem usar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e158b-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e158b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e158b-116">Requirements</span></span>



| <span data-ttu-id="e158b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e158b-117">Requirement</span></span> | <span data-ttu-id="e158b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e158b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e158b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e158b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e158b-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e158b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e158b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e158b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e158b-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e158b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e158b-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e158b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e158b-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e158b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e158b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e158b-126">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="e158b-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="e158b-127">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="e158b-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="e158b-128">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="e158b-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




