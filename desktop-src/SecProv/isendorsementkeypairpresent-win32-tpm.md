---
description: O método IsEndorsementKeyPairPresent da classe Win32 \_ TPM indica se o par de chaves de endosso existe no dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Método IsEndorsementKeyPairPresent da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091790"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="8a729-103">Método IsEndorsementKeyPairPresent da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="8a729-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8a729-104">O método **IsEndorsementKeyPairPresent** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o par de chaves de endosso existe no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a729-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="8a729-105">O par de chaves de endosso é necessário antes que o dispositivo possa ser proprietário.</span><span class="sxs-lookup"><span data-stu-id="8a729-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="8a729-106">Esse par de chaves pode ser criado pelo método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="8a729-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="8a729-107">O dispositivo deve ser habilitado e ativado para que esse método seja bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="8a729-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="8a729-108">Para habilitar e ativar um dispositivo sem proprietário, consulte o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="8a729-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a729-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a729-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="8a729-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a729-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a729-111">*IsEndorsementKeyPairPresent* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8a729-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a729-112">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8a729-112">Type: **boolean**</span></span>

<span data-ttu-id="8a729-113">Se **for true**, o par de chaves de endosso existirá no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a729-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a729-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a729-114">Return value</span></span>

<span data-ttu-id="8a729-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a729-115">Type: **uint32**</span></span>

<span data-ttu-id="8a729-116">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="8a729-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8a729-117">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="8a729-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="8a729-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8a729-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="8a729-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a729-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8a729-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8a729-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8a729-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8a729-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a729-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a729-122">Remarks</span></span>

<span data-ttu-id="8a729-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8a729-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8a729-124">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8a729-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8a729-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8a729-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8a729-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8a729-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a729-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a729-127">Requirements</span></span>



| <span data-ttu-id="8a729-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a729-128">Requirement</span></span> | <span data-ttu-id="8a729-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8a729-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a729-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a729-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a729-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a729-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8a729-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a729-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a729-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a729-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8a729-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a729-134">Namespace</span></span><br/>                | <span data-ttu-id="8a729-135">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="8a729-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8a729-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8a729-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a729-137"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="8a729-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a729-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8a729-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a729-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="8a729-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a729-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a729-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a729-141">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8a729-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="8a729-142">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="8a729-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="8a729-143">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="8a729-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
