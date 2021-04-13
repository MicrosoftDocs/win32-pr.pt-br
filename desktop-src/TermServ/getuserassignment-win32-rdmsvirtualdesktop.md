---
title: Método GetUserAssignment da classe Win32_RDMSVirtualDesktop
description: Recupera o nome de usuário e o domínio que é atribuído à área de trabalho virtual.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetUserAssignment
- Método GetUserAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369737"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="c0f29-106">Método GetUserAssignment da classe Win32 \_ RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="c0f29-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="c0f29-107">Recupera o nome de usuário e o domínio que é atribuído à área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="c0f29-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f29-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0f29-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="c0f29-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0f29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f29-110">*Nome de usuário* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0f29-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f29-111">Recebe o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="c0f29-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="c0f29-112">*UserDomain* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0f29-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f29-113">Recebe o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="c0f29-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f29-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0f29-114">Return value</span></span>

<span data-ttu-id="c0f29-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="c0f29-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f29-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0f29-116">Requirements</span></span>



| <span data-ttu-id="c0f29-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0f29-117">Requirement</span></span> | <span data-ttu-id="c0f29-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c0f29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f29-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0f29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f29-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c0f29-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c0f29-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0f29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f29-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0f29-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c0f29-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0f29-123">Namespace</span></span><br/>                | <span data-ttu-id="c0f29-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="c0f29-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c0f29-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c0f29-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0f29-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0f29-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0f29-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f29-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f29-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f29-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c0f29-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0f29-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f29-130">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="c0f29-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





