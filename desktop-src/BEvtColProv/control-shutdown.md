---
description: Interrompe o coletor. Se o coletor estiver sendo executado como um serviço, a interrupção do serviço será a melhor abordagem.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Método Shutdown da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753849"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="3a898-104">Método Shutdown da classe Control</span><span class="sxs-lookup"><span data-stu-id="3a898-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="3a898-105">Interrompe o coletor.</span><span class="sxs-lookup"><span data-stu-id="3a898-105">Stops the collector.</span></span> <span data-ttu-id="3a898-106">Se o coletor estiver sendo executado como um serviço, a interrupção do serviço será a melhor abordagem.</span><span class="sxs-lookup"><span data-stu-id="3a898-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a898-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a898-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="3a898-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a898-108">Parameters</span></span>

<span data-ttu-id="3a898-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3a898-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a898-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a898-110">Return value</span></span>

<span data-ttu-id="3a898-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3a898-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a898-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a898-112">Requirements</span></span>



| <span data-ttu-id="3a898-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a898-113">Requirement</span></span> | <span data-ttu-id="3a898-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3a898-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a898-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a898-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3a898-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3a898-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3a898-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a898-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3a898-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3a898-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="3a898-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a898-119">Namespace</span></span><br/>                | <span data-ttu-id="3a898-120">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="3a898-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="3a898-121">MOF</span><span class="sxs-lookup"><span data-stu-id="3a898-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a898-122"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a898-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a898-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3a898-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a898-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a898-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3a898-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a898-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a898-126">**Controlo**</span><span class="sxs-lookup"><span data-stu-id="3a898-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




