---
description: Coloca o serviço convidado em um estado iniciado.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Método Msvm_GuestService:: StartService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758793"
---
# <a name="msvm_guestservicestartservice-method"></a><span data-ttu-id="71817-103">\_Método Msvm GuestService:: StartService</span><span class="sxs-lookup"><span data-stu-id="71817-103">Msvm\_GuestService::StartService method</span></span>

<span data-ttu-id="71817-104">Coloca o serviço convidado em um estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="71817-104">Puts the guest service in a started state.</span></span>

## <a name="syntax"></a><span data-ttu-id="71817-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71817-105">Syntax</span></span>


```C++
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="71817-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71817-106">Parameters</span></span>

<span data-ttu-id="71817-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="71817-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71817-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71817-108">Return value</span></span>

<span data-ttu-id="71817-109">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="71817-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="71817-110">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="71817-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="71817-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="71817-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="71817-112"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="71817-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="71817-113">Êxito.</span><span class="sxs-lookup"><span data-stu-id="71817-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="71817-114"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="71817-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="71817-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71817-115">Requirements</span></span>



| <span data-ttu-id="71817-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="71817-116">Requirement</span></span> | <span data-ttu-id="71817-117">Valor</span><span class="sxs-lookup"><span data-stu-id="71817-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71817-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71817-118">Minimum supported client</span></span><br/> | <span data-ttu-id="71817-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71817-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="71817-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71817-120">Minimum supported server</span></span><br/> | <span data-ttu-id="71817-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="71817-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="71817-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="71817-122">Namespace</span></span><br/>                | <span data-ttu-id="71817-123">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="71817-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="71817-124">MOF</span><span class="sxs-lookup"><span data-stu-id="71817-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71817-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71817-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71817-126">DLL</span><span class="sxs-lookup"><span data-stu-id="71817-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71817-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71817-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71817-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="71817-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71817-129">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="71817-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




