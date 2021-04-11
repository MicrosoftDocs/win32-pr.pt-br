---
description: O método IsOwnershipAllowed da classe Win32 \_ TPM indica se a capacidade de instalar um proprietário para o dispositivo é permitida.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Método IsOwnershipAllowed da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164388"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="bc73b-103">Método IsOwnershipAllowed da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="bc73b-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="bc73b-104">O método **IsOwnershipAllowed** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se a capacidade de instalar um proprietário para o dispositivo é permitida.</span><span class="sxs-lookup"><span data-stu-id="bc73b-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc73b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc73b-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="bc73b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc73b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc73b-107">*IsOwnershipAllowed* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bc73b-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc73b-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bc73b-108">Type: **boolean**</span></span>

<span data-ttu-id="bc73b-109">Se for **true**, a capacidade de instalar um proprietário para o dispositivo será permitida.</span><span class="sxs-lookup"><span data-stu-id="bc73b-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="bc73b-110">Se **for false**, o método [**TakeOwnership**](takeownership-win32-tpm.md) falhará ao instalar um proprietário para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc73b-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="bc73b-111">Esse valor pode ser alterado com o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="bc73b-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="bc73b-112">O valor é redefinido como **true** depois que o método [**Clear**](clear-win32-tpm.md) é executado.</span><span class="sxs-lookup"><span data-stu-id="bc73b-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc73b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc73b-113">Return value</span></span>

<span data-ttu-id="bc73b-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc73b-114">Type: **uint32**</span></span>

<span data-ttu-id="bc73b-115">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="bc73b-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="bc73b-116">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="bc73b-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="bc73b-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bc73b-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="bc73b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc73b-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bc73b-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bc73b-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bc73b-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bc73b-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc73b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc73b-121">Remarks</span></span>

<span data-ttu-id="bc73b-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bc73b-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bc73b-123">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc73b-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bc73b-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="bc73b-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bc73b-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bc73b-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc73b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc73b-126">Requirements</span></span>



| <span data-ttu-id="bc73b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc73b-127">Requirement</span></span> | <span data-ttu-id="bc73b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="bc73b-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc73b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc73b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bc73b-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc73b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bc73b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc73b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bc73b-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc73b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bc73b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc73b-133">Namespace</span></span><br/>                | <span data-ttu-id="bc73b-134">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bc73b-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="bc73b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="bc73b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc73b-136"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="bc73b-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc73b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bc73b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc73b-138"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="bc73b-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc73b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc73b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc73b-140">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="bc73b-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
