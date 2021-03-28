---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar o tipo de janela do Gerenciador de arquivos que tem o foco de entrada.
title: Mensagem de FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967946"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="fde88-103">Mensagem do FM \_ GETfocus</span><span class="sxs-lookup"><span data-stu-id="fde88-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="fde88-104">Enviado por uma extensão do Gerenciador de arquivos para recuperar o tipo de janela do Gerenciador de arquivos que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fde88-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="fde88-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fde88-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde88-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fde88-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fde88-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fde88-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fde88-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fde88-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fde88-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fde88-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde88-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fde88-110">Return value</span></span>

<span data-ttu-id="fde88-111">Retorna o tipo da janela do Gerenciador de arquivos que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fde88-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="fde88-112">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="fde88-112">It can be one of the following values.</span></span>



| <span data-ttu-id="fde88-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fde88-113">Return code</span></span>                                                                                    | <span data-ttu-id="fde88-114">Description</span><span class="sxs-lookup"><span data-stu-id="fde88-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="fde88-115"><dt>**FMFOCUS \_ dir**</dt></span><span class="sxs-lookup"><span data-stu-id="fde88-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="fde88-116">Parte do diretório de uma janela de diretório.</span><span class="sxs-lookup"><span data-stu-id="fde88-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="fde88-117"><dt>**árvore de FMFOCUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fde88-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="fde88-118">Parte de árvore de uma janela de diretório.</span><span class="sxs-lookup"><span data-stu-id="fde88-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="fde88-119"><dt>**\_unidades FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="fde88-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="fde88-120">Barra de unidades de uma janela de diretório.</span><span class="sxs-lookup"><span data-stu-id="fde88-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="fde88-121"><dt>**pesquisa do FMFOCUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fde88-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="fde88-122">Janela resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fde88-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="fde88-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde88-123">Requirements</span></span>



| <span data-ttu-id="fde88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde88-124">Requirement</span></span> | <span data-ttu-id="fde88-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fde88-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fde88-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fde88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fde88-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fde88-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fde88-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fde88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fde88-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fde88-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fde88-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fde88-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde88-131"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde88-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




