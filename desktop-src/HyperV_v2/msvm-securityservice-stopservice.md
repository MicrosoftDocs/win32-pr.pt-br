---
description: Método StopService da classe Msvm_SecurityService-para o serviço.
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Método StopService da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a9a16fef951fdee5ed7fc580da61f43d848a8dec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118704"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="dbc67-103">Método StopService da classe Msvm \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="dbc67-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="dbc67-104">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="dbc67-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbc67-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="dbc67-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbc67-106">Parameters</span></span>

<span data-ttu-id="dbc67-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dbc67-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbc67-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dbc67-108">Return value</span></span>

<span data-ttu-id="dbc67-109">Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="dbc67-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="dbc67-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dbc67-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbc67-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="dbc67-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dbc67-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc67-112">Requirements</span></span>



| <span data-ttu-id="dbc67-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc67-113">Requirement</span></span> | <span data-ttu-id="dbc67-114">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc67-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc67-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbc67-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc67-116">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="dbc67-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dbc67-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbc67-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc67-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dbc67-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dbc67-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbc67-119">Namespace</span></span><br/>                | <span data-ttu-id="dbc67-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dbc67-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dbc67-121">MOF</span><span class="sxs-lookup"><span data-stu-id="dbc67-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbc67-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbc67-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbc67-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dbc67-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbc67-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbc67-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbc67-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dbc67-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc67-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="dbc67-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




