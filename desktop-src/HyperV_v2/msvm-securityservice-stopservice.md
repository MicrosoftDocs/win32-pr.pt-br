---
description: Interrompe o serviço.
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
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170257"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="876c9-103">Método StopService da classe Msvm \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="876c9-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="876c9-104">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="876c9-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="876c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="876c9-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="876c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="876c9-106">Parameters</span></span>

<span data-ttu-id="876c9-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="876c9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="876c9-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="876c9-108">Return value</span></span>

<span data-ttu-id="876c9-109">Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="876c9-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="876c9-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="876c9-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="876c9-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="876c9-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="876c9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="876c9-112">Requirements</span></span>



| <span data-ttu-id="876c9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="876c9-113">Requirement</span></span> | <span data-ttu-id="876c9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="876c9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="876c9-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="876c9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="876c9-116">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="876c9-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="876c9-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="876c9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="876c9-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="876c9-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="876c9-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="876c9-119">Namespace</span></span><br/>                | <span data-ttu-id="876c9-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="876c9-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="876c9-121">MOF</span><span class="sxs-lookup"><span data-stu-id="876c9-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="876c9-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="876c9-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="876c9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="876c9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="876c9-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="876c9-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="876c9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="876c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876c9-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="876c9-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




