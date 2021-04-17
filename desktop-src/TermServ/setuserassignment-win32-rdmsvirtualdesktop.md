---
title: Método SetUserAssignment da classe Win32_RDMSVirtualDesktop
description: Atribui uma área de trabalho virtual a um usuário.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserAssignment
- Método SetUserAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770446"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="d2493-106">Método SetUserAssignment da classe Win32 \_ RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="d2493-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="d2493-107">Atribui uma área de trabalho virtual a um usuário.</span><span class="sxs-lookup"><span data-stu-id="d2493-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2493-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2493-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="d2493-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2493-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2493-110">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2493-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2493-111">O nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="d2493-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="d2493-112">*UserDomain* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2493-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2493-113">O nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="d2493-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2493-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2493-114">Return value</span></span>

<span data-ttu-id="d2493-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="d2493-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2493-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2493-116">Requirements</span></span>



| <span data-ttu-id="d2493-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2493-117">Requirement</span></span> | <span data-ttu-id="d2493-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d2493-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2493-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2493-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2493-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d2493-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d2493-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2493-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2493-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2493-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d2493-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2493-123">Namespace</span></span><br/>                | <span data-ttu-id="d2493-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="d2493-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d2493-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d2493-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2493-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2493-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2493-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d2493-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2493-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2493-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d2493-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2493-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2493-130">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="d2493-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





