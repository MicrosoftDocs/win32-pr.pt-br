---
description: Importa as informações de autorização de proprietário de um TPM que já pertence ao registro do sistema operacional.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Método Win32_Tpm:: ImportOwnerAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920809"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="9ed1e-103">\_Método TPM:: ImportOwnerAuth do Win32</span><span class="sxs-lookup"><span data-stu-id="9ed1e-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="9ed1e-104">Importa as informações de autorização de proprietário de um TPM que já pertence ao registro do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="9ed1e-105">Essa operação primeiro validará se as informações de autorização de proprietário fornecidas estiverem corretas.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="9ed1e-106">Se correto, o método importa essas informações para o registro.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="9ed1e-107">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed1e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ed1e-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="9ed1e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ed1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed1e-110">*OwnerAuth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ed1e-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed1e-111">As informações de autorização de proprietário válidas para o TPM.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed1e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ed1e-112">Return value</span></span>

<span data-ttu-id="9ed1e-113">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="9ed1e-114">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="9ed1e-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9ed1e-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="9ed1e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ed1e-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="9ed1e-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed1e-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9ed1e-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ed1e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ed1e-119">Remarks</span></span>

<span data-ttu-id="9ed1e-120">Esse método é particularmente útil nos cenários em que o TPM está em um "pronto com estado de funcionalidade reduzida" e requer que a importação da autorização do proprietário esteja totalmente pronta ou em cenários de inicialização dupla em que um dos sistemas operacionais tenha proprietário do TPM e as informações de autorização do proprietário do TPM não estejam disponíveis no outro sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="9ed1e-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9ed1e-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9ed1e-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9ed1e-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9ed1e-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9ed1e-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9ed1e-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed1e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ed1e-125">Requirements</span></span>



| <span data-ttu-id="9ed1e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed1e-126">Requirement</span></span> | <span data-ttu-id="9ed1e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9ed1e-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed1e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ed1e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed1e-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9ed1e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ed1e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ed1e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed1e-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9ed1e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9ed1e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ed1e-132">Namespace</span></span><br/>                | <span data-ttu-id="9ed1e-133">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9ed1e-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="9ed1e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9ed1e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ed1e-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="9ed1e-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ed1e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9ed1e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ed1e-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9ed1e-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed1e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ed1e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed1e-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="9ed1e-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
