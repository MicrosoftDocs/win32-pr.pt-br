---
title: Método IMsRdpClientShell ShowTrustedSitesManagementDialog
description: Mostra a caixa de diálogo lista de sites confiáveis.
ms.assetid: 8fe84160-386a-415c-a447-7a62f674cdcc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ShowTrustedSitesManagementDialog
- Método ShowTrustedSitesManagementDialog Serviços de Área de Trabalho Remota, interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell, método ShowTrustedSitesManagementDialog
topic_type:
- apiref
api_name:
- IMsRdpClientShell.ShowTrustedSitesManagementDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999ba3a834fa1c4b8c498fb002ddf4d4b1ad5615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644876"
---
# <a name="imsrdpclientshellshowtrustedsitesmanagementdialog-method"></a><span data-ttu-id="1e0ae-106">Método IMsRdpClientShell:: ShowTrustedSitesManagementDialog</span><span class="sxs-lookup"><span data-stu-id="1e0ae-106">IMsRdpClientShell::ShowTrustedSitesManagementDialog method</span></span>

<span data-ttu-id="1e0ae-107">Mostra a caixa de diálogo lista de sites confiáveis.</span><span class="sxs-lookup"><span data-stu-id="1e0ae-107">Shows the list of trusted sites dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e0ae-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e0ae-108">Syntax</span></span>


```C++
HRESULT ShowTrustedSitesManagementDialog();
```



## <a name="parameters"></a><span data-ttu-id="1e0ae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e0ae-109">Parameters</span></span>

<span data-ttu-id="1e0ae-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e0ae-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e0ae-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e0ae-111">Return value</span></span>

<span data-ttu-id="1e0ae-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e0ae-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e0ae-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e0ae-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0ae-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e0ae-114">Requirements</span></span>



| <span data-ttu-id="1e0ae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e0ae-115">Requirement</span></span> | <span data-ttu-id="1e0ae-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1e0ae-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0ae-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e0ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e0ae-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0ae-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1e0ae-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e0ae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1e0ae-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e0ae-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1e0ae-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1e0ae-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e0ae-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e0ae-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e0ae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1e0ae-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e0ae-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e0ae-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e0ae-125">IID</span><span class="sxs-lookup"><span data-stu-id="1e0ae-125">IID</span></span><br/>                      | <span data-ttu-id="1e0ae-126">IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="1e0ae-126">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="1e0ae-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e0ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0ae-128">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="1e0ae-128">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





