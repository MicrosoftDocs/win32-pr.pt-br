---
title: Método GetVirtualDesktopDetails da classe Win32_RDMSVirtualDesktop
description: Recupera as informações adicionais sobre a área de trabalho virtual.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetVirtualDesktopDetails
- Método GetVirtualDesktopDetails Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455389"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="56ff0-106">Método GetVirtualDesktopDetails da classe Win32 \_ RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="56ff0-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="56ff0-107">Recupera as informações adicionais sobre a área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="56ff0-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ff0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56ff0-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="56ff0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56ff0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ff0-110">*RAMSizeInMB* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="56ff0-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ff0-111">Recebe a quantidade de RAM atribuída à área de trabalho virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="56ff0-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="56ff0-112">*RemoteFXEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="56ff0-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ff0-113">Recebe um valor que indica se o RemoteFX está habilitado na área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="56ff0-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="56ff0-114">**True** se o RemoteFX estiver habilitado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="56ff0-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="56ff0-115">*OSVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="56ff0-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ff0-116">Recebe a versão do sistema operacional da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="56ff0-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ff0-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56ff0-117">Return value</span></span>

<span data-ttu-id="56ff0-118">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="56ff0-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ff0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ff0-119">Requirements</span></span>



| <span data-ttu-id="56ff0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ff0-120">Requirement</span></span> | <span data-ttu-id="56ff0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="56ff0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ff0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56ff0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56ff0-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="56ff0-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="56ff0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56ff0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56ff0-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56ff0-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="56ff0-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="56ff0-126">Namespace</span></span><br/>                | <span data-ttu-id="56ff0-127">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="56ff0-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="56ff0-128">MOF</span><span class="sxs-lookup"><span data-stu-id="56ff0-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56ff0-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56ff0-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="56ff0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="56ff0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ff0-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ff0-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="56ff0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="56ff0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ff0-133">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="56ff0-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





