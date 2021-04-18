---
description: Solicita que o dispositivo restabeleça a configuração, a configuração e/ou as informações de estado de um repositório de backup.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Método restoreproperties da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811880"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="15202-103">Método restoreproperties da classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="15202-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="15202-104">Solicita que o dispositivo restabeleça a configuração, a configuração e/ou as informações de estado de um repositório de backup.</span><span class="sxs-lookup"><span data-stu-id="15202-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="15202-105">A intenção é capturar essas informações em um momento anterior (por meio do método SaveProperties) e usá-las para retornar um dispositivo para essa "condição" anterior.</span><span class="sxs-lookup"><span data-stu-id="15202-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="15202-106">Esse método pode não ter suporte de todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="15202-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="15202-107">O método deve retornar 0 se for bem-sucedido, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="15202-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="15202-108">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método.</span><span class="sxs-lookup"><span data-stu-id="15202-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="15202-109">As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="15202-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="15202-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15202-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="15202-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15202-111">Parameters</span></span>

<span data-ttu-id="15202-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15202-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="15202-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15202-113">Requirements</span></span>



| <span data-ttu-id="15202-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15202-114">Requirement</span></span> | <span data-ttu-id="15202-115">Valor</span><span class="sxs-lookup"><span data-stu-id="15202-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15202-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15202-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15202-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="15202-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="15202-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15202-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15202-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="15202-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="15202-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="15202-120">Namespace</span></span><br/>                | <span data-ttu-id="15202-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="15202-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15202-122">MOF</span><span class="sxs-lookup"><span data-stu-id="15202-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15202-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15202-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15202-124">DLL</span><span class="sxs-lookup"><span data-stu-id="15202-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15202-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15202-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15202-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="15202-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15202-127">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="15202-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




