---
description: Recupera os certificados do sistema em um sistema host.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Método GetSystemCertificates da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501385"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="13ee1-103">Método GetSystemCertificates da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="13ee1-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="13ee1-104">Recupera os certificados do sistema em um sistema host.</span><span class="sxs-lookup"><span data-stu-id="13ee1-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ee1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13ee1-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="13ee1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13ee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ee1-107">*EncodedCertificates* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="13ee1-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13ee1-108">Se for bem-sucedido, o receberá os certificados disponíveis do repositório pessoal para o computador local.</span><span class="sxs-lookup"><span data-stu-id="13ee1-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="13ee1-109">Cada entrada é uma cadeia de caracteres de certificado codificado base 64.</span><span class="sxs-lookup"><span data-stu-id="13ee1-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="13ee1-110">Essa cadeia de caracteres pode ser convertida em uma matriz de bytes construindo um objeto X509Certificate2.</span><span class="sxs-lookup"><span data-stu-id="13ee1-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ee1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13ee1-111">Return value</span></span>

<span data-ttu-id="13ee1-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="13ee1-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="13ee1-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="13ee1-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="13ee1-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="13ee1-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="13ee1-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="13ee1-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="13ee1-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="13ee1-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="13ee1-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="13ee1-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="13ee1-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="13ee1-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="13ee1-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="13ee1-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="13ee1-126">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="13ee1-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13ee1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ee1-127">Requirements</span></span>



| <span data-ttu-id="13ee1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ee1-128">Requirement</span></span> | <span data-ttu-id="13ee1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="13ee1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ee1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ee1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13ee1-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="13ee1-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13ee1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ee1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13ee1-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="13ee1-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13ee1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="13ee1-134">Namespace</span></span><br/>                | <span data-ttu-id="13ee1-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="13ee1-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13ee1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="13ee1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13ee1-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13ee1-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13ee1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="13ee1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ee1-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13ee1-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13ee1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="13ee1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ee1-141">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="13ee1-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




