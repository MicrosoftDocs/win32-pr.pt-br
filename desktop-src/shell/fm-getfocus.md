---
description: Enviado por uma extensão do Gerenciador de Arquivos para recuperar o tipo de janela do Gerenciador de Arquivos que tem o foco de entrada.
title: FM_GETFOCUS mensagem (Wfext.h)
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
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841407"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="c2693-103">Mensagem \_ FM GETFOCUS</span><span class="sxs-lookup"><span data-stu-id="c2693-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="c2693-104">Enviado por uma extensão do Gerenciador de Arquivos para recuperar o tipo de janela do Gerenciador de Arquivos que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2693-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2693-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2693-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2693-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2693-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2693-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2693-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2693-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2693-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c2693-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2693-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2693-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2693-110">Return value</span></span>

<span data-ttu-id="c2693-111">Retorna o tipo de janela do Gerenciador de Arquivos que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2693-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="c2693-112">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="c2693-112">It can be one of the following values.</span></span>



| <span data-ttu-id="c2693-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c2693-113">Return code</span></span>                                                                                    | <span data-ttu-id="c2693-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2693-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="c2693-115"><dt>**FMFOCUS \_ DIR**</dt></span><span class="sxs-lookup"><span data-stu-id="c2693-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="c2693-116">Parte do diretório de uma janela de diretório.</span><span class="sxs-lookup"><span data-stu-id="c2693-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="c2693-117"><dt>**ÁRVORE \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="c2693-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="c2693-118">Parte da árvore de uma janela de diretório.</span><span class="sxs-lookup"><span data-stu-id="c2693-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="c2693-119"><dt>**UNIDADES \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="c2693-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="c2693-120">Barra de unidade de uma janela de diretório.</span><span class="sxs-lookup"><span data-stu-id="c2693-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="c2693-121"><dt>**PESQUISA DE \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="c2693-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="c2693-122">Janela Resultados da Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2693-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="c2693-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2693-123">Requirements</span></span>



| <span data-ttu-id="c2693-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2693-124">Requirement</span></span> | <span data-ttu-id="c2693-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c2693-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2693-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2693-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c2693-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2693-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c2693-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2693-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c2693-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2693-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2693-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2693-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2693-131"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="c2693-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




