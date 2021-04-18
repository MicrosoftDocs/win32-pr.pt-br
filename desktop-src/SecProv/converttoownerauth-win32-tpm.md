---
description: Converte uma entrada de senha fornecida pelo usuário em uma autorização de proprietário de 20 bytes que pode ser usada para interagir com o TPM. Métodos como TakeOwnership e ResetAuthLockOut exigem o valor de autorização do proprietário resultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Método ConvertToOwnerAuth da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788094"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="4cabc-104">Método ConvertToOwnerAuth da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="4cabc-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="4cabc-105">O método **ConvertToOwnerAuth** da classe [**\_ TPM do Win32**](win32-tpm.md) converte uma entrada de senha fornecida pelo usuário em uma autorização de proprietário de 20 bytes que pode ser usada para interagir com o TPM.</span><span class="sxs-lookup"><span data-stu-id="4cabc-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="4cabc-106">Métodos como [**TakeOwnership**](takeownership-win32-tpm.md) e [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) exigem o valor de autorização do proprietário resultante.</span><span class="sxs-lookup"><span data-stu-id="4cabc-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="4cabc-107">O processo de conversão segue as especificações do [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span><span class="sxs-lookup"><span data-stu-id="4cabc-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="4cabc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cabc-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="4cabc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cabc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cabc-110">*OwnerPassPhrase* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cabc-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4cabc-111">Type: **string**</span></span>

<span data-ttu-id="4cabc-112">Uma cadeia de caracteres a ser convertida em um valor de autorização de proprietário.</span><span class="sxs-lookup"><span data-stu-id="4cabc-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="4cabc-113">A cadeia de caracteres pode conter qualquer número de caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="4cabc-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="4cabc-114">*OwnerAuth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cabc-115">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4cabc-115">Type: **string**</span></span>

<span data-ttu-id="4cabc-116">Uma cadeia de caracteres derivada do parâmetro *OwnerPassPhrase* .</span><span class="sxs-lookup"><span data-stu-id="4cabc-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="4cabc-117">Esse valor é um valor binário de 20 bytes codificado para uma cadeia de **caracteres com final de Base64 de** 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="4cabc-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cabc-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cabc-118">Return value</span></span>

<span data-ttu-id="4cabc-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cabc-119">Type: **uint32**</span></span>

<span data-ttu-id="4cabc-120">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="4cabc-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="4cabc-121">As tabelas a seguir listam alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="4cabc-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="4cabc-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4cabc-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4cabc-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cabc-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4cabc-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4cabc-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4cabc-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4cabc-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cabc-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cabc-126">Remarks</span></span>

<span data-ttu-id="4cabc-127">Uma cadeia de caracteres codificada em UTF-16LE Unicode é convertida para o valor de autorização de proprietário do TPM de 20 bytes por meio do hash SHA-1 da representação binária da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4cabc-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="4cabc-128">A terminação **nula** da cadeia de caracteres Unicode não está incluída no hash.</span><span class="sxs-lookup"><span data-stu-id="4cabc-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="4cabc-129">Nenhum Salt é usado no hash SHA-1.</span><span class="sxs-lookup"><span data-stu-id="4cabc-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="4cabc-130">Por exemplo, para converter a frase secreta do proprietário do TPM "1Sample" em um valor de autorização de proprietário do TPM, o hash SHA-1 é obtido do seguinte fluxo de bytes:</span><span class="sxs-lookup"><span data-stu-id="4cabc-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="4cabc-131">Para converter uma senha de comprimento zero em um valor de autorização de proprietário, o hash SHA-1 é tirado do fluxo de bytes **nulo** .</span><span class="sxs-lookup"><span data-stu-id="4cabc-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="4cabc-132">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4cabc-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4cabc-133">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="4cabc-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4cabc-134">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="4cabc-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4cabc-135">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4cabc-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cabc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cabc-136">Requirements</span></span>



| <span data-ttu-id="4cabc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cabc-137">Requirement</span></span> | <span data-ttu-id="4cabc-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4cabc-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cabc-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cabc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4cabc-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4cabc-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cabc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4cabc-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4cabc-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cabc-143">Namespace</span></span><br/>                | <span data-ttu-id="4cabc-144">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="4cabc-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="4cabc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="4cabc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cabc-146"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="4cabc-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cabc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4cabc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cabc-148"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="4cabc-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cabc-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cabc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cabc-150">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4cabc-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="4cabc-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="4cabc-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 
