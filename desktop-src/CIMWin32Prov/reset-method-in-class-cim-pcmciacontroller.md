---
description: O método reset da classe CIM \_ PCMCIAController solicita uma redefinição do dispositivo lógico.
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: Método Reset da classe CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164047"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a><span data-ttu-id="5c74e-103">Método Reset da classe CIM \_ PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="5c74e-103">Reset method of the CIM\_PCMCIAController class</span></span>

<span data-ttu-id="5c74e-104">O método **Reset** da classe CIM \_ PCMCIAController solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c74e-104">The **Reset** method of the CIM\_PCMCIAController class requests a reset of the logical device.</span></span> <span data-ttu-id="5c74e-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c74e-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c74e-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5c74e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5c74e-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5c74e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5c74e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c74e-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="5c74e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c74e-109">Parameters</span></span>

<span data-ttu-id="5c74e-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5c74e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c74e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c74e-111">Return value</span></span>

<span data-ttu-id="5c74e-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="5c74e-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c74e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c74e-113">Remarks</span></span>

<span data-ttu-id="5c74e-114">Esse método não é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5c74e-114">This method is not implemented by WMI.</span></span> <span data-ttu-id="5c74e-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="5c74e-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="5c74e-116">Para classes WMI derivadas do [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md), consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5c74e-116">For WMI classes derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5c74e-117">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5c74e-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5c74e-118">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5c74e-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c74e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c74e-119">Requirements</span></span>



| <span data-ttu-id="5c74e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c74e-120">Requirement</span></span> | <span data-ttu-id="5c74e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5c74e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c74e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c74e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c74e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c74e-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c74e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c74e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c74e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c74e-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c74e-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c74e-126">Namespace</span></span><br/>                | <span data-ttu-id="5c74e-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5c74e-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c74e-128">MOF</span><span class="sxs-lookup"><span data-stu-id="5c74e-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c74e-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c74e-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c74e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5c74e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c74e-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c74e-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c74e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c74e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c74e-133">\_PCMCIACONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="5c74e-133">CIM\_PCMCIAController</span></span>](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="5c74e-134">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="5c74e-134">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> </dl>

 

 




