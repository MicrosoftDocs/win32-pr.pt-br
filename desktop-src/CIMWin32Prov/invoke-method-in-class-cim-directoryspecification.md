---
description: O método Invoke da classe CIM \_ DirectorySpecification avalia uma verificação específica.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_DirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48e5cb315f7dba6be187280ee6a16d7c4711752f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811158"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a><span data-ttu-id="a2f42-103">Método Invoke da classe CIM \_ DirectorySpecification</span><span class="sxs-lookup"><span data-stu-id="a2f42-103">Invoke method of the CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="a2f42-104">O método **Invoke** da classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) avalia uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="a2f42-104">The **Invoke** method of the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class evaluates a particular check.</span></span> <span data-ttu-id="a2f42-105">Os detalhes sobre como o método avalia uma verificação específica em um contexto CIM são descritos pelas subclasses de [**\_ verificação CIM**](cim-check.md) não abstratas.</span><span class="sxs-lookup"><span data-stu-id="a2f42-105">Details about how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="a2f42-106">Esse método é herdado **da \_ verificação CIM**.</span><span class="sxs-lookup"><span data-stu-id="a2f42-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2f42-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a2f42-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a2f42-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a2f42-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a2f42-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a2f42-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a2f42-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a2f42-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f42-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2f42-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a2f42-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2f42-112">Parameters</span></span>

<span data-ttu-id="a2f42-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a2f42-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2f42-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2f42-114">Return value</span></span>

<span data-ttu-id="a2f42-115">Retorna um 0 se for bem-sucedido, um 1 se o método não tiver suporte e qualquer outro valor indicará um erro.</span><span class="sxs-lookup"><span data-stu-id="a2f42-115">Returns a 0 if successful, a 1 if the method is not supported, and any other value indicates an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2f42-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2f42-116">Remarks</span></span>

<span data-ttu-id="a2f42-117">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="a2f42-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a2f42-118">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="a2f42-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a2f42-119">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a2f42-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a2f42-120">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a2f42-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f42-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2f42-121">Requirements</span></span>



| <span data-ttu-id="a2f42-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2f42-122">Requirement</span></span> | <span data-ttu-id="a2f42-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a2f42-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f42-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2f42-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a2f42-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2f42-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2f42-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2f42-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a2f42-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2f42-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2f42-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2f42-128">Namespace</span></span><br/>                | <span data-ttu-id="a2f42-129">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a2f42-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2f42-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a2f42-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2f42-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2f42-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2f42-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a2f42-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2f42-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2f42-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f42-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2f42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f42-135">\_DIRECTORYSPECIFICATION CIM</span><span class="sxs-lookup"><span data-stu-id="a2f42-135">CIM\_DirectorySpecification</span></span>](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[<span data-ttu-id="a2f42-136">**\_DIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="a2f42-136">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> </dl>

 

