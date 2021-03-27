---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar informações de unidade da janela do Active File Manager.
title: Mensagem de FM_GETDRIVEINFO (Wfext. h)
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
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988739"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="e3a2c-103">Mensagem do FM \_ GETdriveinfo</span><span class="sxs-lookup"><span data-stu-id="e3a2c-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="e3a2c-104">Enviado por uma extensão do Gerenciador de arquivos para recuperar informações de unidade da janela do Active File Manager.</span><span class="sxs-lookup"><span data-stu-id="e3a2c-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3a2c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a2c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a2c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3a2c-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e3a2c-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e3a2c-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e3a2c-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="e3a2c-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a2c-109">O endereço de uma [**estrutura \_ GetDriveInfo do FMS**](fms-getdriveinfo.md) que recebe informações da unidade.</span><span class="sxs-lookup"><span data-stu-id="e3a2c-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a2c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3a2c-110">Return value</span></span>

<span data-ttu-id="e3a2c-111">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="e3a2c-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a2c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a2c-112">Remarks</span></span>

<span data-ttu-id="e3a2c-113">Se 0xFFFFFFFF for retornado no membro **dwTotalSpace** ou **dwFreeSpace** da estrutura [**\_ GetDriveInfo do FMS**](fms-getdriveinfo.md) , a biblioteca de extensões deverá calcular o valor ou os valores.</span><span class="sxs-lookup"><span data-stu-id="e3a2c-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a2c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a2c-114">Requirements</span></span>



| <span data-ttu-id="e3a2c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a2c-115">Requirement</span></span> | <span data-ttu-id="e3a2c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e3a2c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a2c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3a2c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a2c-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3a2c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e3a2c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3a2c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a2c-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3a2c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3a2c-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3a2c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a2c-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a2c-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a2c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3a2c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a2c-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="e3a2c-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




