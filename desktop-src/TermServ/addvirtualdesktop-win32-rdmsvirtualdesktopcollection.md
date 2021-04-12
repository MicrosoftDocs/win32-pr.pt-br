---
title: Método AddVirtualDesktop da classe Win32_RDMSVirtualDesktopCollection
description: Adiciona uma área de trabalho virtual à coleção de áreas de trabalho virtuais.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddVirtualDesktop
- Método AddVirtualDesktop Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método AddVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499281"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="512aa-106">Método AddVirtualDesktop da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="512aa-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="512aa-107">Adiciona uma área de trabalho virtual à coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="512aa-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="512aa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="512aa-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="512aa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="512aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="512aa-110">*VMName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="512aa-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512aa-111">O nome da máquina virtual que hospeda a área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="512aa-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="512aa-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="512aa-112">Return value</span></span>

<span data-ttu-id="512aa-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="512aa-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="512aa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="512aa-114">Requirements</span></span>



| <span data-ttu-id="512aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="512aa-115">Requirement</span></span> | <span data-ttu-id="512aa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="512aa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="512aa-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="512aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="512aa-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="512aa-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="512aa-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="512aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="512aa-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="512aa-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="512aa-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="512aa-121">Namespace</span></span><br/>                | <span data-ttu-id="512aa-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="512aa-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="512aa-123">MOF</span><span class="sxs-lookup"><span data-stu-id="512aa-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="512aa-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="512aa-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="512aa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="512aa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="512aa-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="512aa-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="512aa-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="512aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512aa-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="512aa-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





