---
description: Indica se o TPM está pronto para uso.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: 'Método Win32_Tpm:: IsReady'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 37c9d579e424c89f8670838b09ed1c557514ca00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501526"
---
# <a name="win32_tpmisready-method"></a><span data-ttu-id="9a634-103">\_Método TPM:: IsReady do Win32</span><span class="sxs-lookup"><span data-stu-id="9a634-103">Win32\_Tpm::IsReady method</span></span>

<span data-ttu-id="9a634-104">Indica se o TPM está pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="9a634-104">Indicates whether the TPM is ready for use.</span></span>

<span data-ttu-id="9a634-105">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="9a634-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a634-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a634-106">Syntax</span></span>


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a><span data-ttu-id="9a634-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a634-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a634-108">*IsReady* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9a634-108">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a634-109">Defina como **true** se o TPM e o sistema forem totalmente provisionados para uso do TPM.</span><span class="sxs-lookup"><span data-stu-id="9a634-109">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a634-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a634-110">Return value</span></span>

<span data-ttu-id="9a634-111">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="9a634-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="9a634-112">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="9a634-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="9a634-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9a634-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="9a634-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a634-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="9a634-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9a634-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9a634-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9a634-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a634-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a634-117">Remarks</span></span>

<span data-ttu-id="9a634-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9a634-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9a634-119">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9a634-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9a634-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9a634-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9a634-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9a634-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a634-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a634-122">Requirements</span></span>



| <span data-ttu-id="9a634-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a634-123">Requirement</span></span> | <span data-ttu-id="9a634-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9a634-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a634-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a634-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a634-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9a634-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a634-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a634-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a634-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9a634-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9a634-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a634-129">Namespace</span></span><br/>                | <span data-ttu-id="9a634-130">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9a634-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="9a634-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9a634-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a634-132"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="9a634-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a634-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9a634-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a634-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9a634-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a634-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a634-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a634-136">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="9a634-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
