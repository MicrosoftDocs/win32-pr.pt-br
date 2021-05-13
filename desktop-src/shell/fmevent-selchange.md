---
description: Enviado a uma DLL de extensão quando o usuário seleciona um nome de arquivo na janela do diretório do Gerenciador de arquivos ou na janela de resultados da pesquisa.
title: Mensagem de FMEVENT_SELCHANGE (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: e9aa647434aab5a483626757179a7b23b3372a02
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842257"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="d74ec-103">\_Mensagem FMEVENT SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="d74ec-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="d74ec-104">Enviado a uma DLL de extensão quando o usuário seleciona um nome de arquivo na janela do diretório do Gerenciador de arquivos ou na janela de resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d74ec-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="d74ec-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d74ec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d74ec-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d74ec-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d74ec-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d74ec-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d74ec-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d74ec-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d74ec-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d74ec-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d74ec-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d74ec-110">Return value</span></span>

<span data-ttu-id="d74ec-111">Uma DLL de extensão deve retornar zero se ela processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="d74ec-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d74ec-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d74ec-112">Remarks</span></span>

<span data-ttu-id="d74ec-113">As alterações na parte da árvore da janela do diretório não produzem essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="d74ec-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="d74ec-114">Como o usuário pode alterar a seleção várias vezes, a DLL de extensão deve retornar imediatamente após o processamento dessa mensagem para evitar a lentidão do processo de seleção para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d74ec-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="d74ec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d74ec-115">Requirements</span></span>



| <span data-ttu-id="d74ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d74ec-116">Requirement</span></span> | <span data-ttu-id="d74ec-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d74ec-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d74ec-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d74ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d74ec-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d74ec-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d74ec-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d74ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d74ec-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d74ec-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d74ec-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d74ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d74ec-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="d74ec-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d74ec-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d74ec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74ec-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="d74ec-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




