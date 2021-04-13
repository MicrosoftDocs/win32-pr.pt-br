---
title: Método de inicialização IMsRdpClientShell
description: Inicia o conteúdo do arquivo remoto de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de algum outro portal da Web.
ms.assetid: a0aa12e4-8b6f-4a3a-a6b8-f5def0b8bd90
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de inicialização
- Método de inicialização Serviços de Área de Trabalho Remota, interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell, método de inicialização
topic_type:
- apiref
api_name:
- IMsRdpClientShell.Launch
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae895d8a12824c6aca1dcbd69c5055b3ca6f3e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369375"
---
# <a name="imsrdpclientshelllaunch-method"></a><span data-ttu-id="90a87-106">Método IMsRdpClientShell:: Launch</span><span class="sxs-lookup"><span data-stu-id="90a87-106">IMsRdpClientShell::Launch method</span></span>

<span data-ttu-id="90a87-107">Inicia o conteúdo do arquivo remoto de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de algum outro portal da Web.</span><span class="sxs-lookup"><span data-stu-id="90a87-107">Launches remote file content from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a87-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90a87-108">Syntax</span></span>


```C++
HRESULT Launch();
```



## <a name="parameters"></a><span data-ttu-id="90a87-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90a87-109">Parameters</span></span>

<span data-ttu-id="90a87-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="90a87-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90a87-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90a87-111">Return value</span></span>

<span data-ttu-id="90a87-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="90a87-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90a87-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90a87-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a87-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a87-114">Requirements</span></span>



| <span data-ttu-id="90a87-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a87-115">Requirement</span></span> | <span data-ttu-id="90a87-116">Valor</span><span class="sxs-lookup"><span data-stu-id="90a87-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90a87-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a87-117">Minimum supported client</span></span><br/> | <span data-ttu-id="90a87-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90a87-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="90a87-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a87-119">Minimum supported server</span></span><br/> | <span data-ttu-id="90a87-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90a87-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="90a87-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="90a87-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="90a87-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90a87-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="90a87-123">DLL</span><span class="sxs-lookup"><span data-stu-id="90a87-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90a87-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90a87-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="90a87-125">IID</span><span class="sxs-lookup"><span data-stu-id="90a87-125">IID</span></span><br/>                      | <span data-ttu-id="90a87-126">IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="90a87-126">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="90a87-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a87-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a87-128">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="90a87-128">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





