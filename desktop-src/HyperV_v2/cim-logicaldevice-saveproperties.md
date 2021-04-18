---
description: Solicita que o dispositivo Capture sua configuração atual, a configuração e/ou as informações de estado em um repositório de backup.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Método SaveProperties da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792529"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="ac5f7-103">Método SaveProperties da classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="ac5f7-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="ac5f7-104">Solicita que o dispositivo Capture sua configuração atual, a configuração e/ou as informações de estado em um repositório de backup.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="ac5f7-105">O objetivo seria usar essas informações mais tarde (por meio do método restoreproperties) para retornar um dispositivo para sua presente "Condition".</span><span class="sxs-lookup"><span data-stu-id="ac5f7-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="ac5f7-106">Esse método pode não ter suporte de todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="ac5f7-107">O método deve retornar 0 se for bem-sucedido, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="ac5f7-108">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="ac5f7-109">As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5f7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac5f7-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="ac5f7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac5f7-111">Parameters</span></span>

<span data-ttu-id="ac5f7-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac5f7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac5f7-113">Return value</span></span>

<span data-ttu-id="ac5f7-114">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ac5f7-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5f7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac5f7-115">Requirements</span></span>



| <span data-ttu-id="ac5f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac5f7-116">Requirement</span></span> | <span data-ttu-id="ac5f7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ac5f7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5f7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac5f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5f7-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ac5f7-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ac5f7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac5f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5f7-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ac5f7-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ac5f7-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac5f7-122">Namespace</span></span><br/>                | <span data-ttu-id="ac5f7-123">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ac5f7-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ac5f7-124">MOF</span><span class="sxs-lookup"><span data-stu-id="ac5f7-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac5f7-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac5f7-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac5f7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ac5f7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac5f7-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac5f7-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac5f7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac5f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5f7-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ac5f7-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




