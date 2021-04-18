---
description: O método Invoke da classe de \_ verificação CIM avalia uma verificação específica.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756251"
---
# <a name="invoke-method-of-the-cim_check-class"></a><span data-ttu-id="b7415-103">Método Invoke da classe de \_ verificação CIM</span><span class="sxs-lookup"><span data-stu-id="b7415-103">Invoke method of the CIM\_Check class</span></span>

<span data-ttu-id="b7415-104">O método **Invoke** da classe [**de \_ verificação CIM**](cim-check.md) avalia uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="b7415-104">The **Invoke** method of the [**CIM\_Check**](cim-check.md) class evaluates a particular check.</span></span>

<span data-ttu-id="b7415-105">Para obter mais informações sobre como o método avalia uma verificação específica em um contexto CIM, consulte as subclasses [**de \_ verificação CIM**](cim-check.md) não abstratas.</span><span class="sxs-lookup"><span data-stu-id="b7415-105">For more information about how the method evaluates a particular check in a CIM context, see the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7415-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b7415-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b7415-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b7415-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b7415-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b7415-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b7415-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b7415-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7415-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7415-110">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="b7415-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7415-111">Parameters</span></span>

<span data-ttu-id="b7415-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b7415-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7415-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7415-113">Return value</span></span>

<span data-ttu-id="b7415-114">Retorna um valor de 0 (zero) em êxito, 1 (um) se o método não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b7415-114">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7415-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7415-115">Remarks</span></span>

<span data-ttu-id="b7415-116">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b7415-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b7415-117">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="b7415-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b7415-118">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b7415-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b7415-119">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b7415-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7415-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7415-120">Requirements</span></span>



| <span data-ttu-id="b7415-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7415-121">Requirement</span></span> | <span data-ttu-id="b7415-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b7415-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7415-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7415-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b7415-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7415-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7415-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7415-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b7415-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7415-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7415-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7415-127">Namespace</span></span><br/>                | <span data-ttu-id="b7415-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b7415-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7415-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b7415-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7415-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7415-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7415-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b7415-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7415-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7415-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7415-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7415-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7415-134">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b7415-134">**CIM\_Check**</span></span>](invoke-method-in-class-cim-check.md)
</dt> <dt>

[<span data-ttu-id="b7415-135">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b7415-135">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

