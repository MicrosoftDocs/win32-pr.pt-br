---
description: Solicita uma redefinição do LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Método Reset da classe CIM_LogicalDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297208"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="7e936-103">Método Reset da classe CIM_LogicalDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7e936-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="7e936-104">Solicita uma redefinição do LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="7e936-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="7e936-105">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método.</span><span class="sxs-lookup"><span data-stu-id="7e936-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="7e936-106">As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="7e936-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e936-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e936-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="7e936-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e936-108">Parameters</span></span>

<span data-ttu-id="7e936-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7e936-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e936-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e936-110">Return value</span></span>

<span data-ttu-id="7e936-111">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7e936-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e936-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e936-112">Requirements</span></span>



| <span data-ttu-id="7e936-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e936-113">Requirement</span></span> | <span data-ttu-id="7e936-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7e936-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e936-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e936-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7e936-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7e936-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7e936-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e936-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7e936-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7e936-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7e936-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e936-119">Namespace</span></span><br/>                | <span data-ttu-id="7e936-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7e936-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e936-121">MOF</span><span class="sxs-lookup"><span data-stu-id="7e936-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e936-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e936-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e936-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7e936-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e936-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e936-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e936-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e936-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e936-126">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7e936-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




