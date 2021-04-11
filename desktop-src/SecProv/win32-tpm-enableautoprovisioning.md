---
description: Habilita o provisionamento automático do TPM se ele estiver desabilitado no momento.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: 'Método Win32_Tpm:: EnableAutoProvisioning'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296262"
---
# <a name="win32_tpmenableautoprovisioning-method"></a><span data-ttu-id="2f86f-103">\_Método TPM:: EnableAutoProvisioning do Win32</span><span class="sxs-lookup"><span data-stu-id="2f86f-103">Win32\_Tpm::EnableAutoProvisioning method</span></span>

<span data-ttu-id="2f86f-104">Habilita o provisionamento automático do TPM se ele estiver desabilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="2f86f-104">Enables auto provisioning of the TPM if it is currently disabled.</span></span> <span data-ttu-id="2f86f-105">A operação não terá efeito se o provisionamento automático já estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="2f86f-105">The operation has no effect if auto provisioning is already enabled.</span></span> <span data-ttu-id="2f86f-106">Por padrão, o provisionamento automático está habilitado para o Windows 8 e o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2f86f-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="2f86f-107">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="2f86f-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f86f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f86f-108">Syntax</span></span>


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a><span data-ttu-id="2f86f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f86f-109">Parameters</span></span>

<span data-ttu-id="2f86f-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2f86f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f86f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f86f-111">Return value</span></span>

<span data-ttu-id="2f86f-112">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="2f86f-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="2f86f-113">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="2f86f-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="2f86f-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2f86f-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="2f86f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f86f-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2f86f-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2f86f-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="2f86f-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2f86f-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f86f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f86f-118">Remarks</span></span>

<span data-ttu-id="2f86f-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2f86f-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2f86f-120">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2f86f-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2f86f-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="2f86f-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2f86f-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2f86f-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f86f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f86f-123">Requirements</span></span>



| <span data-ttu-id="2f86f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f86f-124">Requirement</span></span> | <span data-ttu-id="2f86f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2f86f-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f86f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f86f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2f86f-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f86f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f86f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f86f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2f86f-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f86f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2f86f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f86f-130">Namespace</span></span><br/>                | <span data-ttu-id="2f86f-131">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2f86f-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="2f86f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2f86f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f86f-133"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="2f86f-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f86f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2f86f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f86f-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="2f86f-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f86f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f86f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f86f-137">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2f86f-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
