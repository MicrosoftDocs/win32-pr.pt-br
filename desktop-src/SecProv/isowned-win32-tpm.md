---
description: O método isdele da \_ classe TPM do Win32 indica se o dispositivo tem um proprietário. Esse valor é alterado pelo método TakeOwnership.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Método isdelel da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501530"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="9fb17-104">Método isdelery da \_ classe TPM do Win32</span><span class="sxs-lookup"><span data-stu-id="9fb17-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9fb17-105">O **método isdele da** classe [**\_ TPM do Win32**](win32-tpm.md) indica se o dispositivo tem um proprietário.</span><span class="sxs-lookup"><span data-stu-id="9fb17-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="9fb17-106">Esse valor é alterado pelo método [**TakeOwnership**](takeownership-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb17-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb17-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fb17-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="9fb17-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fb17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb17-109">Isdele  \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9fb17-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb17-110">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9fb17-110">Type: **boolean**</span></span>

<span data-ttu-id="9fb17-111">Se **for true**, o dispositivo terá um proprietário.</span><span class="sxs-lookup"><span data-stu-id="9fb17-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb17-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fb17-112">Return value</span></span>

<span data-ttu-id="9fb17-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fb17-113">Type: **uint32**</span></span>

<span data-ttu-id="9fb17-114">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="9fb17-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9fb17-115">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="9fb17-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="9fb17-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9fb17-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="9fb17-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fb17-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="9fb17-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9fb17-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9fb17-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9fb17-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9fb17-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fb17-120">Remarks</span></span>

<span data-ttu-id="9fb17-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9fb17-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9fb17-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fb17-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9fb17-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9fb17-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9fb17-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9fb17-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb17-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb17-125">Requirements</span></span>



| <span data-ttu-id="9fb17-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb17-126">Requirement</span></span> | <span data-ttu-id="9fb17-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9fb17-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb17-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb17-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb17-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fb17-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9fb17-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb17-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb17-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fb17-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9fb17-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fb17-132">Namespace</span></span><br/>                | <span data-ttu-id="9fb17-133">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9fb17-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9fb17-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb17-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb17-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="9fb17-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb17-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9fb17-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb17-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9fb17-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb17-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fb17-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb17-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="9fb17-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
