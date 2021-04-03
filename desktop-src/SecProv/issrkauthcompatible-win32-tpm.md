---
description: O método IsSrkAuthCompatible da classe Win32 \_ TPM indica se a autorização da chave de raiz de armazenamento (SRK) é compatível com o valor esperado pelo Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Método IsSrkAuthCompatible da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829308"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="aeef6-103">Método IsSrkAuthCompatible da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="aeef6-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="aeef6-104">O método **IsSrkAuthCompatible** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se a autorização da chave de raiz de armazenamento (SRK) é compatível com o valor esperado pelo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aeef6-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeef6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aeef6-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="aeef6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeef6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeef6-107">*IsSrkAuthCompatible* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aeef6-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeef6-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="aeef6-108">Type: **boolean**</span></span>

<span data-ttu-id="aeef6-109">Se **for true**, o valor de autorização de SRK terá um valor igual a zero.</span><span class="sxs-lookup"><span data-stu-id="aeef6-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeef6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aeef6-110">Return value</span></span>

<span data-ttu-id="aeef6-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeef6-111">Type: **uint32**</span></span>

<span data-ttu-id="aeef6-112">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="aeef6-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="aeef6-113">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="aeef6-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="aeef6-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aeef6-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="aeef6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="aeef6-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="aeef6-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="aeef6-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="aeef6-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aeef6-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aeef6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeef6-118">Remarks</span></span>

<span data-ttu-id="aeef6-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="aeef6-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aeef6-120">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="aeef6-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="aeef6-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="aeef6-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aeef6-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="aeef6-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aeef6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeef6-123">Requirements</span></span>



| <span data-ttu-id="aeef6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeef6-124">Requirement</span></span> | <span data-ttu-id="aeef6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="aeef6-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeef6-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeef6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aeef6-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aeef6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aeef6-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeef6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aeef6-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aeef6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="aeef6-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="aeef6-130">Namespace</span></span><br/>                | <span data-ttu-id="aeef6-131">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="aeef6-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="aeef6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="aeef6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeef6-133"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="aeef6-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeef6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="aeef6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeef6-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="aeef6-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeef6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeef6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeef6-137">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="aeef6-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
