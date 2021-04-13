---
description: Obtém as informações de autorização do proprietário de um TPM, se houver um disponível no registro.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Método Win32_Tpm:: GetOwnerAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501527"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="36b1c-103">\_Método TPM:: GetOwnerAuth do Win32</span><span class="sxs-lookup"><span data-stu-id="36b1c-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="36b1c-104">Obtém as informações de autorização do proprietário de um TPM, se houver um disponível no registro.</span><span class="sxs-lookup"><span data-stu-id="36b1c-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="36b1c-105">Se um TPM for proprietário ou provisionado no Windows 8 com as configurações padrão, as informações de autorização do proprietário do TPM serão armazenadas no registro e estarão disponíveis para uso por esse método.</span><span class="sxs-lookup"><span data-stu-id="36b1c-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="36b1c-106">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="36b1c-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b1c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36b1c-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="36b1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36b1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36b1c-109">*OwnerAuth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="36b1c-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36b1c-110">As informações de autorização do proprietário de um TPM, se houver uma disponível no registro.</span><span class="sxs-lookup"><span data-stu-id="36b1c-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36b1c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36b1c-111">Return value</span></span>

<span data-ttu-id="36b1c-112">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="36b1c-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="36b1c-113">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="36b1c-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="36b1c-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="36b1c-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="36b1c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="36b1c-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="36b1c-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="36b1c-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="36b1c-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="36b1c-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36b1c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="36b1c-118">Remarks</span></span>

<span data-ttu-id="36b1c-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="36b1c-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="36b1c-120">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="36b1c-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="36b1c-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="36b1c-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="36b1c-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="36b1c-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36b1c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36b1c-123">Requirements</span></span>



| <span data-ttu-id="36b1c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="36b1c-124">Requirement</span></span> | <span data-ttu-id="36b1c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="36b1c-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="36b1c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36b1c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="36b1c-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="36b1c-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36b1c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36b1c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="36b1c-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="36b1c-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="36b1c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="36b1c-130">Namespace</span></span><br/>                | <span data-ttu-id="36b1c-131">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="36b1c-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="36b1c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="36b1c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36b1c-133"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="36b1c-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="36b1c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="36b1c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36b1c-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="36b1c-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b1c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="36b1c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b1c-137">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="36b1c-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
