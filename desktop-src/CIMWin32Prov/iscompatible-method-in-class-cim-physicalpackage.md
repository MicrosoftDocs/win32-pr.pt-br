---
description: Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Método iscompatível da classe CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752962"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="87676-103">Método iscompatível da classe CIM \_ PhysicalPackage</span><span class="sxs-lookup"><span data-stu-id="87676-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="87676-104">O método **iscompatível** verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="87676-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="87676-105">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="87676-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="87676-106">As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="87676-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87676-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="87676-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="87676-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="87676-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="87676-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="87676-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="87676-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="87676-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="87676-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87676-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="87676-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87676-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87676-113">*ElementToCheck* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87676-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87676-114">Referência ao elemento físico no qual o método **iscompatível** é executado.</span><span class="sxs-lookup"><span data-stu-id="87676-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87676-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87676-115">Return value</span></span>

<span data-ttu-id="87676-116">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="87676-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="87676-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="87676-117">Remarks</span></span>

<span data-ttu-id="87676-118">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="87676-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="87676-119">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="87676-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="87676-120">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="87676-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="87676-121">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="87676-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="87676-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87676-122">Requirements</span></span>



| <span data-ttu-id="87676-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="87676-123">Requirement</span></span> | <span data-ttu-id="87676-124">Valor</span><span class="sxs-lookup"><span data-stu-id="87676-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87676-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87676-125">Minimum supported client</span></span><br/> | <span data-ttu-id="87676-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87676-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87676-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87676-127">Minimum supported server</span></span><br/> | <span data-ttu-id="87676-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87676-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87676-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="87676-129">Namespace</span></span><br/>                | <span data-ttu-id="87676-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="87676-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87676-131">MOF</span><span class="sxs-lookup"><span data-stu-id="87676-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87676-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87676-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87676-133">DLL</span><span class="sxs-lookup"><span data-stu-id="87676-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87676-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87676-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87676-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="87676-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87676-136">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="87676-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="87676-137">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="87676-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

