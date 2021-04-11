---
description: O método QuiesceDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Método QuiesceDevice da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297210"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="ae7c4-103">Método QuiesceDevice da classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="ae7c4-103">QuiesceDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="ae7c4-104">O método **QuiesceDevice** foi preterido no lugar do método **RequestStateChange** mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.</span><span class="sxs-lookup"><span data-stu-id="ae7c4-104">The **QuiesceDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae7c4-105">Syntax</span></span>


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a><span data-ttu-id="ae7c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae7c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7c4-107">*Desativar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae7c4-107">*Quiesce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7c4-108">Se definido como **true** , interrompa corretamente todas as atividades, se **false** retomar a atividade.</span><span class="sxs-lookup"><span data-stu-id="ae7c4-108">If set to **TRUE** then cleanly cease all activity, if **FALSE** resume activity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7c4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae7c4-109">Return value</span></span>

<span data-ttu-id="ae7c4-110">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ae7c4-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7c4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae7c4-111">Requirements</span></span>



| <span data-ttu-id="ae7c4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7c4-112">Requirement</span></span> | <span data-ttu-id="ae7c4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ae7c4-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7c4-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae7c4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae7c4-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ae7c4-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ae7c4-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae7c4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae7c4-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ae7c4-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ae7c4-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae7c4-118">Namespace</span></span><br/>                | <span data-ttu-id="ae7c4-119">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ae7c4-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae7c4-120">MOF</span><span class="sxs-lookup"><span data-stu-id="ae7c4-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae7c4-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae7c4-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae7c4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ae7c4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae7c4-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae7c4-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae7c4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae7c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7c4-125">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ae7c4-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




