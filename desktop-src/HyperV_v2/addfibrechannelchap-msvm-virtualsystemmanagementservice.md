---
description: Adiciona parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a uma porta de Fibre Channel sintética em uma máquina virtual.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Método AddFibreChannelChap da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921787"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="93bd9-103">Método AddFibreChannelChap da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="93bd9-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="93bd9-104">Adiciona parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a uma porta de Fibre Channel sintética em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93bd9-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="93bd9-105">Esse método falhará se a máquina virtual estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="93bd9-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bd9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93bd9-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="93bd9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93bd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bd9-108">*FcPortSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93bd9-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bd9-109">Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que descreve as configurações de portas Fibre Channel sintéticas para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="93bd9-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="93bd9-110">A propriedade **InstanceId** de cada uma dessas instâncias identifica os elementos a serem modificados.</span><span class="sxs-lookup"><span data-stu-id="93bd9-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="93bd9-111">*SecretEncoding* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93bd9-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bd9-112">Especifica o tipo de codificação para o segredo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="93bd9-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="93bd9-113">**ASCII imprimível** (1)</span><span class="sxs-lookup"><span data-stu-id="93bd9-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="93bd9-114">**Binário** (2)</span><span class="sxs-lookup"><span data-stu-id="93bd9-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="93bd9-115">*SharedSecret* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93bd9-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bd9-116">Especifica o segredo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="93bd9-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bd9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93bd9-117">Return value</span></span>

<span data-ttu-id="93bd9-118">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="93bd9-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="93bd9-119">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="93bd9-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="93bd9-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="93bd9-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="93bd9-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="93bd9-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="93bd9-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="93bd9-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="93bd9-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="93bd9-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="93bd9-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="93bd9-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="93bd9-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="93bd9-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="93bd9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93bd9-131">Requirements</span></span>



| <span data-ttu-id="93bd9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="93bd9-132">Requirement</span></span> | <span data-ttu-id="93bd9-133">Valor</span><span class="sxs-lookup"><span data-stu-id="93bd9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bd9-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93bd9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="93bd9-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="93bd9-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93bd9-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93bd9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="93bd9-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="93bd9-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93bd9-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="93bd9-138">Namespace</span></span><br/>                | <span data-ttu-id="93bd9-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="93bd9-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93bd9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="93bd9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93bd9-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93bd9-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93bd9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="93bd9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93bd9-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93bd9-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93bd9-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="93bd9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bd9-145">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="93bd9-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




