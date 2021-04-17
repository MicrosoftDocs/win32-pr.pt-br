---
description: Altera a credencial de autorização do proprietário do dispositivo TPM. As senhas de autorização de proprietário antigo e novo são necessárias.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Método ChangeOwnerAuth da classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770226"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="6ee11-104">Método ChangeOwnerAuth da classe CIM \_ TPM</span><span class="sxs-lookup"><span data-stu-id="6ee11-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="6ee11-105">Altera a credencial de autorização do proprietário do dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="6ee11-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="6ee11-106">As senhas de autorização de proprietário antigo e novo são necessárias.</span><span class="sxs-lookup"><span data-stu-id="6ee11-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee11-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ee11-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="6ee11-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ee11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee11-109">*OldOwnerAuth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ee11-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee11-110">Representa a credencial de autorização de proprietário antiga necessária para apropriar-se do dispositivo TPM. A subclasse **CIM \_ SharedCredential** pode ser necessária com um valor não nulo do **\_ SharedCredential CIM**.**Propriedade secreta** para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ee11-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6ee11-111">*NewOwnerAuth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ee11-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee11-112">Representa a nova credencial de autorização de proprietário necessária para apropriar-se do dispositivo TPM. A subclasse **CIM \_ SharedCredential** pode ser necessária com um valor não nulo do **\_ SharedCredential CIM**.**Propriedade secreta** para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ee11-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee11-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ee11-113">Return value</span></span>

<span data-ttu-id="6ee11-114">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6ee11-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6ee11-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="6ee11-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6ee11-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6ee11-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6ee11-117">**Erro desconhecido/não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="6ee11-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6ee11-118">**DMTF reservado** (3.. 4095)</span><span class="sxs-lookup"><span data-stu-id="6ee11-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="6ee11-119">**Método reservado** (4096.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6ee11-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6ee11-120">**Fornecedor especificado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6ee11-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6ee11-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee11-121">Requirements</span></span>



| <span data-ttu-id="6ee11-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee11-122">Requirement</span></span> | <span data-ttu-id="6ee11-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee11-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee11-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ee11-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee11-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6ee11-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6ee11-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ee11-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee11-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6ee11-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6ee11-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ee11-128">Namespace</span></span><br/>                | <span data-ttu-id="6ee11-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6ee11-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ee11-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6ee11-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ee11-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ee11-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ee11-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee11-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee11-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ee11-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ee11-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ee11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee11-135">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="6ee11-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




