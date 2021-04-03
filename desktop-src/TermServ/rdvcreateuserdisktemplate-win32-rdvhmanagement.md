---
title: Método RdvCreateUserDiskTemplate da classe Win32_RdvhManagement
description: Cria um modelo de disco de usuário, com o tamanho máximo especificado, no local especificado.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvCreateUserDiskTemplate
- Método RdvCreateUserDiskTemplate Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvCreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645096"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="5efc5-106">Método RdvCreateUserDiskTemplate da classe Win32 \_ RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="5efc5-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="5efc5-107">Cria um modelo de disco de usuário, com o tamanho máximo especificado, no local especificado.</span><span class="sxs-lookup"><span data-stu-id="5efc5-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="5efc5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5efc5-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="5efc5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5efc5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5efc5-110">*UserDisksStorageUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5efc5-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5efc5-111">Local do armazenamento em disco do usuário.</span><span class="sxs-lookup"><span data-stu-id="5efc5-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="5efc5-112">*UserDiskMaxSizeInGB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5efc5-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5efc5-113">Tamanho máximo do disco do usuário, em GB.</span><span class="sxs-lookup"><span data-stu-id="5efc5-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5efc5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5efc5-114">Return value</span></span>

<span data-ttu-id="5efc5-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="5efc5-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5efc5-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="5efc5-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5efc5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5efc5-117">Remarks</span></span>

<span data-ttu-id="5efc5-118">Todos os discos de usuário criados usando esse modelo terão o mesmo tamanho máximo que o modelo.</span><span class="sxs-lookup"><span data-stu-id="5efc5-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="5efc5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5efc5-119">Requirements</span></span>



| <span data-ttu-id="5efc5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5efc5-120">Requirement</span></span> | <span data-ttu-id="5efc5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5efc5-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5efc5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5efc5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5efc5-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5efc5-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="5efc5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5efc5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5efc5-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5efc5-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="5efc5-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5efc5-126">Namespace</span></span><br/>                | <span data-ttu-id="5efc5-127">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5efc5-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="5efc5-128">MOF</span><span class="sxs-lookup"><span data-stu-id="5efc5-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5efc5-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5efc5-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5efc5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5efc5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5efc5-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5efc5-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5efc5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5efc5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5efc5-133">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="5efc5-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





