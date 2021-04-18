---
title: Método RemoveUserAssignment da classe Win32_RDMSVirtualDesktop
description: Remove a atribuição de usuário da área de trabalho virtual.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveUserAssignment
- Método RemoveUserAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788029"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="08be3-106">Método RemoveUserAssignment da classe Win32 \_ RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="08be3-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="08be3-107">Remove a atribuição de usuário da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="08be3-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="08be3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08be3-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="08be3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08be3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08be3-110">*VMName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08be3-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08be3-111">O nome da máquina virtual da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="08be3-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08be3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08be3-112">Return value</span></span>

<span data-ttu-id="08be3-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="08be3-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="08be3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08be3-114">Requirements</span></span>



| <span data-ttu-id="08be3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="08be3-115">Requirement</span></span> | <span data-ttu-id="08be3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="08be3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08be3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08be3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08be3-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="08be3-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="08be3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08be3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08be3-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08be3-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="08be3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="08be3-121">Namespace</span></span><br/>                | <span data-ttu-id="08be3-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="08be3-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="08be3-123">MOF</span><span class="sxs-lookup"><span data-stu-id="08be3-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08be3-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08be3-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="08be3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="08be3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08be3-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08be3-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="08be3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="08be3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08be3-128">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="08be3-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





