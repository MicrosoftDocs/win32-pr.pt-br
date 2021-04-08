---
description: Verifica se o quadro físico referenciado pode ser contido ou inserido no pacote físico.
ms.assetid: 8102569d-a956-445a-ae42-23eb206ba224
ms.tgt_platform: multiple
title: Método iscompatível da classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 121405e66a9361e832f6accb24ca6e303bb8e280
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920283"
---
# <a name="iscompatible-method-of-the-cim_physicalframe-class"></a><span data-ttu-id="8e5f4-103">Método iscompatível da classe CIM \_ PhysicalFrame</span><span class="sxs-lookup"><span data-stu-id="8e5f4-103">IsCompatible method of the CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="8e5f4-104">O método **iscompatível** verifica se o quadro físico referenciado pode ser contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-104">The **IsCompatible** method verifies whether the referenced physical frame can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="8e5f4-105">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="8e5f4-106">As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="8e5f4-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="8e5f4-107">Esse método é herdado do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e5f4-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e5f4-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e5f4-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e5f4-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e5f4-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8e5f4-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e5f4-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e5f4-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5f4-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e5f4-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="8e5f4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e5f4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e5f4-114">*ElementToCheck* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e5f4-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5f4-115">Referência ao elemento físico no qual o método **iscompatível** é executado.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e5f4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e5f4-116">Return value</span></span>

<span data-ttu-id="8e5f4-117">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e5f4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e5f4-118">Remarks</span></span>

<span data-ttu-id="8e5f4-119">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8e5f4-120">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8e5f4-121">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e5f4-122">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5f4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e5f4-123">Requirements</span></span>



| <span data-ttu-id="8e5f4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5f4-124">Requirement</span></span> | <span data-ttu-id="8e5f4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8e5f4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5f4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e5f4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5f4-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e5f4-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e5f4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e5f4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5f4-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e5f4-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e5f4-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e5f4-130">Namespace</span></span><br/>                | <span data-ttu-id="8e5f4-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e5f4-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e5f4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8e5f4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e5f4-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e5f4-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e5f4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8e5f4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e5f4-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e5f4-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5f4-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e5f4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5f4-137">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="8e5f4-137">**CIM\_PhysicalFrame**</span></span>](iscompatible-method-in-class-cim-physicalframe.md)
</dt> <dt>

[<span data-ttu-id="8e5f4-138">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="8e5f4-138">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

