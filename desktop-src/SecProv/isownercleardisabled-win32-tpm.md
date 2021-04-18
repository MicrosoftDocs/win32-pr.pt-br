---
description: O método IsOwnerClearDisabled da classe Win32 \_ TPM indica se o proprietário do dispositivo está restrito à limpeza do dispositivo.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Método IsOwnerClearDisabled da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800065"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="b462e-103">Método IsOwnerClearDisabled da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="b462e-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b462e-104">O método **IsOwnerClearDisabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o proprietário do dispositivo está restrito à limpeza do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b462e-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b462e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b462e-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="b462e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b462e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b462e-107">*IsOwnerClearDisabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b462e-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b462e-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b462e-108">Type: **boolean**</span></span>

<span data-ttu-id="b462e-109">Se for **true**, o proprietário do dispositivo não poderá limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b462e-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="b462e-110">Somente um usuário fisicamente presente pode ser capaz de limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b462e-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="b462e-111">Se for **false**, o proprietário do dispositivo poderá limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b462e-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b462e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b462e-112">Return value</span></span>

<span data-ttu-id="b462e-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b462e-113">Type: **uint32**</span></span>

<span data-ttu-id="b462e-114">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b462e-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b462e-115">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="b462e-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="b462e-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b462e-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="b462e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b462e-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b462e-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="b462e-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b462e-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b462e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b462e-120">Remarks</span></span>

<span data-ttu-id="b462e-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b462e-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b462e-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b462e-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b462e-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b462e-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b462e-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b462e-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b462e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b462e-125">Requirements</span></span>



| <span data-ttu-id="b462e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b462e-126">Requirement</span></span> | <span data-ttu-id="b462e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b462e-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b462e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b462e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b462e-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b462e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b462e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b462e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b462e-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b462e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b462e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b462e-132">Namespace</span></span><br/>                | <span data-ttu-id="b462e-133">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b462e-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b462e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b462e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b462e-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b462e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b462e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b462e-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b462e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b462e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b462e-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="b462e-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
