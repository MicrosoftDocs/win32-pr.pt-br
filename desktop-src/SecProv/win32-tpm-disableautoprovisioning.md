---
description: Desabilita o provisionamento automático do TPM se ele estiver habilitado no momento.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D método isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756374"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="c8a7d-103">TPM do Win32 \_ : método de:D isableautoprovisioning</span><span class="sxs-lookup"><span data-stu-id="c8a7d-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="c8a7d-104">Desabilita o provisionamento automático do TPM se ele estiver habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="c8a7d-105">A operação não terá efeito se o provisionamento automático já estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="c8a7d-106">Por padrão, o provisionamento automático está habilitado para o Windows 8 e o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="c8a7d-107">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a7d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8a7d-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="c8a7d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8a7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a7d-110">*OnlyForNextBoot* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c8a7d-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8a7d-111">Se definido como **true**, o provisionamento automático será desabilitado apenas para a próxima inicialização.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="c8a7d-112">Se definido como **false** ou não for especificado, o provisionamento automático será permanentemente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a7d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8a7d-113">Return value</span></span>

<span data-ttu-id="c8a7d-114">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="c8a7d-115">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="c8a7d-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c8a7d-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c8a7d-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8a7d-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c8a7d-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8a7d-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8a7d-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8a7d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8a7d-120">Remarks</span></span>

<span data-ttu-id="c8a7d-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c8a7d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c8a7d-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c8a7d-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c8a7d-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c8a7d-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a7d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8a7d-125">Requirements</span></span>



| <span data-ttu-id="c8a7d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a7d-126">Requirement</span></span> | <span data-ttu-id="c8a7d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c8a7d-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a7d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8a7d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a7d-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c8a7d-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8a7d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8a7d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a7d-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c8a7d-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c8a7d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8a7d-132">Namespace</span></span><br/>                | <span data-ttu-id="c8a7d-133">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c8a7d-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="c8a7d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c8a7d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8a7d-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="c8a7d-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8a7d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a7d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8a7d-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="c8a7d-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a7d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8a7d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a7d-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="c8a7d-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
