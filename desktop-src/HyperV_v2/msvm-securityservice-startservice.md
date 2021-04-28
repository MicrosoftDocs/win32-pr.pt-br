---
description: Método StartService da classe Msvm_SecurityService – inicia o serviço.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Método StartService da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111394"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="3a772-103">Método StartService da classe Msvm \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="3a772-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="3a772-104">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="3a772-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a772-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a772-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="3a772-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a772-106">Parameters</span></span>

<span data-ttu-id="3a772-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3a772-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a772-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3a772-108">Return value</span></span>

<span data-ttu-id="3a772-109">Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3a772-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3a772-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3a772-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a772-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3a772-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3a772-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a772-112">Requirements</span></span>



| <span data-ttu-id="3a772-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a772-113">Requirement</span></span> | <span data-ttu-id="3a772-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3a772-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a772-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a772-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3a772-116">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="3a772-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3a772-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a772-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3a772-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3a772-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3a772-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a772-119">Namespace</span></span><br/>                | <span data-ttu-id="3a772-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3a772-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a772-121">MOF</span><span class="sxs-lookup"><span data-stu-id="3a772-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a772-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a772-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a772-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3a772-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a772-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a772-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a772-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3a772-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a772-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="3a772-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




