---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa).
title: Mensagem de FM_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828303"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="df130-103">\_Mensagem GETFILESEL de FM</span><span class="sxs-lookup"><span data-stu-id="df130-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="df130-104">Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="df130-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="df130-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df130-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df130-106">*index*</span><span class="sxs-lookup"><span data-stu-id="df130-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="df130-107">O índice de base zero do arquivo selecionado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="df130-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="df130-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="df130-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="df130-109">O endereço de uma [**estrutura \_ GETFILESEL do FMS**](fms-getfilesel.md) que recebe informações sobre a seleção.</span><span class="sxs-lookup"><span data-stu-id="df130-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df130-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df130-110">Return value</span></span>

<span data-ttu-id="df130-111">Retorna o índice de base zero do arquivo selecionado que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="df130-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="df130-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="df130-112">Remarks</span></span>

<span data-ttu-id="df130-113">Uma extensão pode usar a [**mensagem \_ GETSELCOUNT de FM**](fm-getselcount.md) para recuperar a contagem de arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="df130-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="df130-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df130-114">Requirements</span></span>



| <span data-ttu-id="df130-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="df130-115">Requirement</span></span> | <span data-ttu-id="df130-116">Valor</span><span class="sxs-lookup"><span data-stu-id="df130-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df130-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df130-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df130-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df130-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="df130-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df130-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df130-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df130-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df130-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df130-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="df130-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="df130-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df130-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="df130-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df130-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="df130-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="df130-125">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="df130-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="df130-126">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="df130-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




