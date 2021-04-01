---
description: Indica se o provisionamento automático do TPM está habilitado.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Método Win32_Tpm:: IsAutoProvisioningEnabled'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829303"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="97463-103">\_Método TPM:: IsAutoProvisioningEnabled do Win32</span><span class="sxs-lookup"><span data-stu-id="97463-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="97463-104">Indica se o provisionamento automático do TPM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="97463-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="97463-105">Por padrão, o provisionamento automático está habilitado para o Windows 8 e o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="97463-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="97463-106">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="97463-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="97463-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97463-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="97463-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97463-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97463-109">*IsAutoProvisioningEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="97463-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97463-110">Defina como **true** se o provisionamento automático do TPM estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="97463-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97463-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97463-111">Return value</span></span>

<span data-ttu-id="97463-112">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="97463-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="97463-113">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="97463-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="97463-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="97463-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="97463-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="97463-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="97463-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="97463-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="97463-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="97463-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97463-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="97463-118">Remarks</span></span>

<span data-ttu-id="97463-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="97463-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="97463-120">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="97463-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="97463-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="97463-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="97463-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="97463-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97463-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97463-123">Requirements</span></span>



| <span data-ttu-id="97463-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="97463-124">Requirement</span></span> | <span data-ttu-id="97463-125">Valor</span><span class="sxs-lookup"><span data-stu-id="97463-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="97463-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97463-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97463-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97463-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="97463-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97463-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97463-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97463-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="97463-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="97463-130">Namespace</span></span><br/>                | <span data-ttu-id="97463-131">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="97463-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="97463-132">MOF</span><span class="sxs-lookup"><span data-stu-id="97463-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97463-133"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="97463-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="97463-134">DLL</span><span class="sxs-lookup"><span data-stu-id="97463-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97463-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="97463-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97463-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="97463-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97463-137">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="97463-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
