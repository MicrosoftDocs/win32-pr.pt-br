---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa). O arquivo selecionado pode ter um nome de arquivo longo.
title: Mensagem de FM_GETFILESELLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457206"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="30bea-104">\_Mensagem GETFILESELLFN de FM</span><span class="sxs-lookup"><span data-stu-id="30bea-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="30bea-105">Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="30bea-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="30bea-106">O arquivo selecionado pode ter um nome de arquivo longo.</span><span class="sxs-lookup"><span data-stu-id="30bea-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="30bea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30bea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30bea-108">*index*</span><span class="sxs-lookup"><span data-stu-id="30bea-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="30bea-109">O índice de base zero do arquivo selecionado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="30bea-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="30bea-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="30bea-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="30bea-111">O endereço de uma [**estrutura \_ GETFILESEL do FMS**](fms-getfilesel.md) que recebe informações sobre a seleção.</span><span class="sxs-lookup"><span data-stu-id="30bea-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30bea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30bea-112">Return value</span></span>

<span data-ttu-id="30bea-113">Retorna o índice de base zero do arquivo selecionado que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="30bea-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bea-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="30bea-114">Remarks</span></span>

<span data-ttu-id="30bea-115">Somente extensões que dão suporte a nomes de arquivo longos (por exemplo, extensões com reconhecimento de rede) devem usar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="30bea-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="30bea-116">Uma extensão pode usar a [**mensagem \_ GETSELCOUNTLFN de FM**](fm-getselcountlfn.md) para recuperar a contagem de arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="30bea-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="30bea-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30bea-117">Requirements</span></span>



| <span data-ttu-id="30bea-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30bea-118">Requirement</span></span> | <span data-ttu-id="30bea-119">Valor</span><span class="sxs-lookup"><span data-stu-id="30bea-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30bea-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30bea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30bea-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30bea-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="30bea-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30bea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30bea-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30bea-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="30bea-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="30bea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30bea-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="30bea-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30bea-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="30bea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bea-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="30bea-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="30bea-128">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="30bea-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="30bea-129">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="30bea-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




