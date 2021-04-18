---
title: Método CancelPatch da classe Win32_RDMSVirtualDesktopCollection
description: Cancela um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.
ms.assetid: fb0d6831-5c69-4017-b725-1a5038ad69f5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CancelPatch
- Método CancelPatch Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método CancelPatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.CancelPatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56f33a819da976187fba823ac30fada9ff38730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769389"
---
# <a name="cancelpatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="4b3f7-106">Método CancelPatch da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="4b3f7-106">CancelPatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="4b3f7-107">Cancela um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="4b3f7-107">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b3f7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b3f7-108">Syntax</span></span>


```mof
uint32 CancelPatch();
```



## <a name="parameters"></a><span data-ttu-id="4b3f7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b3f7-109">Parameters</span></span>

<span data-ttu-id="4b3f7-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b3f7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b3f7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b3f7-111">Return value</span></span>

<span data-ttu-id="4b3f7-112">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="4b3f7-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b3f7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b3f7-113">Requirements</span></span>



| <span data-ttu-id="4b3f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b3f7-114">Requirement</span></span> | <span data-ttu-id="4b3f7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4b3f7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3f7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b3f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3f7-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4b3f7-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4b3f7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b3f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3f7-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b3f7-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4b3f7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b3f7-120">Namespace</span></span><br/>                | <span data-ttu-id="4b3f7-121">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="4b3f7-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4b3f7-122">MOF</span><span class="sxs-lookup"><span data-stu-id="4b3f7-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b3f7-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b3f7-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b3f7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4b3f7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b3f7-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b3f7-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4b3f7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b3f7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3f7-127">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="4b3f7-127">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





