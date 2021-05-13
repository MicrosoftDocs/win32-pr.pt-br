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
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841417"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="30b4a-103">\_Mensagem GETFILESEL de FM</span><span class="sxs-lookup"><span data-stu-id="30b4a-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="30b4a-104">Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="30b4a-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="30b4a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30b4a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b4a-106">*index*</span><span class="sxs-lookup"><span data-stu-id="30b4a-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="30b4a-107">O índice de base zero do arquivo selecionado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="30b4a-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="30b4a-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="30b4a-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="30b4a-109">O endereço de uma [**estrutura \_ GETFILESEL do FMS**](fms-getfilesel.md) que recebe informações sobre a seleção.</span><span class="sxs-lookup"><span data-stu-id="30b4a-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b4a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30b4a-110">Return value</span></span>

<span data-ttu-id="30b4a-111">Retorna o índice de base zero do arquivo selecionado que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="30b4a-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b4a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="30b4a-112">Remarks</span></span>

<span data-ttu-id="30b4a-113">Uma extensão pode usar a [**mensagem \_ GETSELCOUNT de FM**](fm-getselcount.md) para recuperar a contagem de arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="30b4a-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b4a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b4a-114">Requirements</span></span>



| <span data-ttu-id="30b4a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b4a-115">Requirement</span></span> | <span data-ttu-id="30b4a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="30b4a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30b4a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30b4a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30b4a-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30b4a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="30b4a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30b4a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30b4a-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30b4a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="30b4a-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="30b4a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b4a-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b4a-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b4a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="30b4a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b4a-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="30b4a-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="30b4a-125">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="30b4a-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="30b4a-126">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="30b4a-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




