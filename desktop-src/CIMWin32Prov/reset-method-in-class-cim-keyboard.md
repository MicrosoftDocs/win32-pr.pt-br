---
description: O método reset da classe de \_ teclado CIM solicita uma redefinição do dispositivo lógico.
ms.assetid: 737bd50c-8e40-4f60-9deb-587b6f37c151
ms.tgt_platform: multiple
title: Método Reset da classe CIM_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Keyboard.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e5296953e157182c97e113539b1b47625a0de44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920452"
---
# <a name="reset-method-of-the-cim_keyboard-class"></a><span data-ttu-id="e52de-103">Método Reset da classe de \_ teclado CIM</span><span class="sxs-lookup"><span data-stu-id="e52de-103">Reset method of the CIM\_Keyboard class</span></span>

<span data-ttu-id="e52de-104">O método **Reset** da classe de \_ teclado CIM solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e52de-104">The **Reset** method of the CIM\_Keyboard class requests a reset of the logical device.</span></span> <span data-ttu-id="e52de-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e52de-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e52de-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e52de-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e52de-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e52de-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e52de-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e52de-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e52de-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e52de-109">Parameters</span></span>

<span data-ttu-id="e52de-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e52de-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e52de-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e52de-111">Return value</span></span>

<span data-ttu-id="e52de-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="e52de-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e52de-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e52de-113">Remarks</span></span>

<span data-ttu-id="e52de-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e52de-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e52de-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="e52de-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e52de-116">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e52de-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e52de-117">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e52de-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e52de-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e52de-118">Requirements</span></span>



| <span data-ttu-id="e52de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e52de-119">Requirement</span></span> | <span data-ttu-id="e52de-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e52de-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e52de-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e52de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e52de-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e52de-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e52de-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e52de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e52de-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e52de-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e52de-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e52de-125">Namespace</span></span><br/>                | <span data-ttu-id="e52de-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e52de-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e52de-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e52de-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e52de-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e52de-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e52de-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e52de-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e52de-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e52de-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e52de-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e52de-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52de-132">\_Teclado CIM</span><span class="sxs-lookup"><span data-stu-id="e52de-132">CIM\_Keyboard</span></span>](reset-method-in-class-cim-keyboard.md)
</dt> <dt>

[<span data-ttu-id="e52de-133">**\_Teclado CIM**</span><span class="sxs-lookup"><span data-stu-id="e52de-133">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> </dl>

 

 




