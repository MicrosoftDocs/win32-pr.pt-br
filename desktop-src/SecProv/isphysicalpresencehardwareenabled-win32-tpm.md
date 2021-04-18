---
description: O método IsPhysicalPresenceHardwareEnabled da classe Win32 \_ TPM indica se a presença física na plataforma pode ser definida com um sinal de hardware.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Método IsPhysicalPresenceHardwareEnabled da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370637"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="95965-103">Método IsPhysicalPresenceHardwareEnabled da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="95965-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="95965-104">O método **IsPhysicalPresenceHardwareEnabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se a presença física na plataforma pode ser definida com um sinal de hardware.</span><span class="sxs-lookup"><span data-stu-id="95965-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="95965-105">Esse valor é configurado pelo fabricante da plataforma com base no design da plataforma.</span><span class="sxs-lookup"><span data-stu-id="95965-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="95965-106">A documentação do fabricante da plataforma pode fornecer informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="95965-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="95965-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95965-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="95965-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95965-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95965-109">*IsPhysicalPresenceHardwareEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95965-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95965-110">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95965-110">Type: **boolean**</span></span>

<span data-ttu-id="95965-111">Se **for true**, a presença física na plataforma poderá ser definida com um sinal de hardware.</span><span class="sxs-lookup"><span data-stu-id="95965-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95965-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95965-112">Return value</span></span>

<span data-ttu-id="95965-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95965-113">Type: **uint32**</span></span>

<span data-ttu-id="95965-114">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="95965-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="95965-115">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="95965-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="95965-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="95965-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="95965-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="95965-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="95965-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95965-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95965-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="95965-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95965-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="95965-120">Remarks</span></span>

<span data-ttu-id="95965-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="95965-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="95965-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="95965-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="95965-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="95965-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="95965-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="95965-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95965-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95965-125">Requirements</span></span>



| <span data-ttu-id="95965-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95965-126">Requirement</span></span> | <span data-ttu-id="95965-127">Valor</span><span class="sxs-lookup"><span data-stu-id="95965-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="95965-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95965-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95965-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95965-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="95965-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95965-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95965-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95965-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="95965-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="95965-132">Namespace</span></span><br/>                | <span data-ttu-id="95965-133">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="95965-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="95965-134">MOF</span><span class="sxs-lookup"><span data-stu-id="95965-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95965-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="95965-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="95965-136">DLL</span><span class="sxs-lookup"><span data-stu-id="95965-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95965-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="95965-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95965-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="95965-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95965-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="95965-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
