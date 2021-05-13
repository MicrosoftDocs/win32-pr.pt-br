---
description: Enviado por uma extensão do Gerenciador de Arquivos para recuperar informações da unidade da janela ativa do Gerenciador de Arquivos.
title: FM_GETDRIVEINFO mensagem (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842407"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="5c714-103">Mensagem \_ FM GETDRIVEINFO</span><span class="sxs-lookup"><span data-stu-id="5c714-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="5c714-104">Enviado por uma extensão do Gerenciador de Arquivos para recuperar informações da unidade da janela ativa do Gerenciador de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="5c714-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c714-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c714-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c714-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c714-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5c714-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5c714-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5c714-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="5c714-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="5c714-109">O endereço de uma estrutura [**\_ GETDRIVEINFO do FMS**](fms-getdriveinfo.md) que recebe informações de unidade.</span><span class="sxs-lookup"><span data-stu-id="5c714-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c714-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c714-110">Return value</span></span>

<span data-ttu-id="5c714-111">Retorna um zero.</span><span class="sxs-lookup"><span data-stu-id="5c714-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c714-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c714-112">Remarks</span></span>

<span data-ttu-id="5c714-113">Se 0xFFFFFFFF for retornado no **membro dwTotalSpace** ou **dwFreeSpace** da estrutura [**\_ GETDRIVEINFO do FMS,**](fms-getdriveinfo.md) a biblioteca de extensões deverá computar o valor ou os valores.</span><span class="sxs-lookup"><span data-stu-id="5c714-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c714-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c714-114">Requirements</span></span>



| <span data-ttu-id="5c714-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c714-115">Requirement</span></span> | <span data-ttu-id="5c714-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5c714-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c714-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c714-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5c714-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c714-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5c714-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c714-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5c714-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c714-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c714-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c714-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c714-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="5c714-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c714-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c714-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c714-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="5c714-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




