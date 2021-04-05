---
description: Interrompe o serviço convidado.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Método Msvm_GuestService:: StopService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827011"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="0df56-103">\_Método Msvm GuestService:: StopService</span><span class="sxs-lookup"><span data-stu-id="0df56-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="0df56-104">Interrompe o serviço convidado.</span><span class="sxs-lookup"><span data-stu-id="0df56-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0df56-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="0df56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0df56-106">Parameters</span></span>

<span data-ttu-id="0df56-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0df56-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0df56-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0df56-108">Return value</span></span>

<span data-ttu-id="0df56-109">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0df56-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="0df56-110">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0df56-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="0df56-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0df56-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="0df56-112"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0df56-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="0df56-113">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0df56-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="0df56-114"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0df56-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="0df56-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0df56-115">Requirements</span></span>



| <span data-ttu-id="0df56-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df56-116">Requirement</span></span> | <span data-ttu-id="0df56-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0df56-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df56-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0df56-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0df56-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0df56-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0df56-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0df56-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0df56-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="0df56-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0df56-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0df56-122">Namespace</span></span><br/>                | <span data-ttu-id="0df56-123">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0df56-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="0df56-124">MOF</span><span class="sxs-lookup"><span data-stu-id="0df56-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0df56-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0df56-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0df56-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0df56-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df56-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0df56-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0df56-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0df56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df56-129">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="0df56-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




