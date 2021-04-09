---
description: Cria uma nova instância de ClusterShare do Win32 \_ .
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Método Create da classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089621"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="e2fa0-103">Método Create da classe Win32 \_ ClusterShare</span><span class="sxs-lookup"><span data-stu-id="e2fa0-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="e2fa0-104">Cria uma nova instância de [**\_ ClusterShare do Win32**](win32-clustershare.md) .</span><span class="sxs-lookup"><span data-stu-id="e2fa0-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fa0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2fa0-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="e2fa0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fa0-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-108">Caminho local do compartilhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-108">Local path of the Windows share.</span></span>

<span data-ttu-id="e2fa0-109">Exemplo, "C: \\ arquivos de programas".</span><span class="sxs-lookup"><span data-stu-id="e2fa0-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-111">O alias para um caminho configurado como um compartilhamento em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="e2fa0-112">Exemplo, "público".</span><span class="sxs-lookup"><span data-stu-id="e2fa0-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-113">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-114">Tipo de recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-114">Type of resource being shared.</span></span> <span data-ttu-id="e2fa0-115">Os tipos incluem: unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="e2fa0-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-117">Unidade de disco</span><span class="sxs-lookup"><span data-stu-id="e2fa0-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-118">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-119">Fila de impressão</span><span class="sxs-lookup"><span data-stu-id="e2fa0-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-120">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-121">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="e2fa0-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-122">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-123">IPC</span><span class="sxs-lookup"><span data-stu-id="e2fa0-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-124">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-125">Administrador da unidade de disco</span><span class="sxs-lookup"><span data-stu-id="e2fa0-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-126">2147483649 (0x80000001)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-127">Administrador da fila de impressão</span><span class="sxs-lookup"><span data-stu-id="e2fa0-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-128">2147483650 (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-129">Administrador do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e2fa0-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-130">2147483651 (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="e2fa0-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-131">Administrador de IPC</span><span class="sxs-lookup"><span data-stu-id="e2fa0-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e2fa0-132">*MaximumAllowed* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-133">Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-134">*Descrição* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-135">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-136">*Senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-137">TBD</span><span class="sxs-lookup"><span data-stu-id="e2fa0-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="e2fa0-138">*Acesso* \[ ao em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2fa0-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fa0-139">Instância incorporada opcional de uma classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) que contém o descritor de segurança para o novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e2fa0-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2fa0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2fa0-140">Requirements</span></span>



| <span data-ttu-id="e2fa0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2fa0-141">Requirement</span></span> | <span data-ttu-id="e2fa0-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e2fa0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fa0-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2fa0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e2fa0-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2fa0-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e2fa0-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2fa0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e2fa0-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2fa0-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e2fa0-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2fa0-147">Namespace</span></span><br/>                | <span data-ttu-id="e2fa0-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e2fa0-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2fa0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e2fa0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2fa0-150"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2fa0-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2fa0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e2fa0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2fa0-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2fa0-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2fa0-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2fa0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fa0-154">**\_ClusterShare Win32**</span><span class="sxs-lookup"><span data-stu-id="e2fa0-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

