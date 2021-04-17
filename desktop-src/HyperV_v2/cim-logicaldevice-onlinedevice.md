---
description: O método OnlineDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Método OnlineDevice da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775741"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="f63e7-103">Método OnlineDevice da classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="f63e7-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="f63e7-104">O método **OnlineDevice** foi preterido no lugar do método **RequestStateChange** mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.</span><span class="sxs-lookup"><span data-stu-id="f63e7-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f63e7-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="f63e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f63e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f63e7-107">*Online* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f63e7-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f63e7-108">Se **for true**, coloque o dispositivo online, se **for false**, coloque o dispositivo offline.</span><span class="sxs-lookup"><span data-stu-id="f63e7-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f63e7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f63e7-109">Return value</span></span>

<span data-ttu-id="f63e7-110">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f63e7-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63e7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f63e7-111">Requirements</span></span>



| <span data-ttu-id="f63e7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63e7-112">Requirement</span></span> | <span data-ttu-id="f63e7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f63e7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63e7-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f63e7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f63e7-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f63e7-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f63e7-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f63e7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f63e7-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f63e7-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f63e7-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f63e7-118">Namespace</span></span><br/>                | <span data-ttu-id="f63e7-119">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f63e7-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f63e7-120">MOF</span><span class="sxs-lookup"><span data-stu-id="f63e7-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f63e7-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f63e7-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f63e7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f63e7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f63e7-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f63e7-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f63e7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f63e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63e7-125">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f63e7-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




