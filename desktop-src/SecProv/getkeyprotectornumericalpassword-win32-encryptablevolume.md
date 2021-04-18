---
description: Recupera a senha numérica de um determinado protetor de chave.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Método GetKeyProtectorNumericalPassword da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105800067"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="673f1-103">Método GetKeyProtectorNumericalPassword da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="673f1-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="673f1-104">O método **GetKeyProtectorNumericalPassword** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera a senha numérica de um determinado protetor de chave do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="673f1-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="673f1-105">O identificador de protetor de chave deve se referir a um protetor de chave do tipo "senha numérica".</span><span class="sxs-lookup"><span data-stu-id="673f1-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="673f1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="673f1-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="673f1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="673f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673f1-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="673f1-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673f1-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="673f1-109">Type: **string**</span></span>

<span data-ttu-id="673f1-110">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="673f1-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="673f1-111">*NumericalPassword* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="673f1-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="673f1-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="673f1-112">Type: **string**</span></span>

<span data-ttu-id="673f1-113">Uma cadeia de caracteres que representa a senha que pode ser usada para desbloquear o volume correspondente.</span><span class="sxs-lookup"><span data-stu-id="673f1-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="673f1-114">A senha numérica é de 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="673f1-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="673f1-115">Esses dígitos são divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo, indicando um valor de soma de verificação para o grupo.</span><span class="sxs-lookup"><span data-stu-id="673f1-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="673f1-116">Supondo que um grupo de seis dígitos seja rotulado como X1, X2, X3, x4, X5 e X6, o dígito de soma de verificação X6 é calculado como – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="673f1-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="673f1-117">Os grupos de dígitos são separados por um hífen.</span><span class="sxs-lookup"><span data-stu-id="673f1-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="673f1-118">Portanto, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" é o formato da senha retornada.</span><span class="sxs-lookup"><span data-stu-id="673f1-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673f1-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="673f1-119">Return value</span></span>

<span data-ttu-id="673f1-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="673f1-120">Type: **uint32**</span></span>

<span data-ttu-id="673f1-121">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="673f1-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="673f1-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="673f1-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="673f1-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="673f1-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="673f1-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="673f1-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="673f1-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="673f1-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="673f1-126"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="673f1-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="673f1-127">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="673f1-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="673f1-128"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="673f1-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="673f1-129">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "senha numérica".</span><span class="sxs-lookup"><span data-stu-id="673f1-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="673f1-130"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="673f1-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="673f1-131">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="673f1-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="673f1-132">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="673f1-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="673f1-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="673f1-133">Remarks</span></span>

<span data-ttu-id="673f1-134">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="673f1-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="673f1-135">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="673f1-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="673f1-136">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="673f1-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="673f1-137">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="673f1-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="673f1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="673f1-138">Requirements</span></span>



| <span data-ttu-id="673f1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="673f1-139">Requirement</span></span> | <span data-ttu-id="673f1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="673f1-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673f1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="673f1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="673f1-142">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="673f1-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="673f1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="673f1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="673f1-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="673f1-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="673f1-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="673f1-145">Namespace</span></span><br/>                | <span data-ttu-id="673f1-146">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="673f1-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="673f1-147">MOF</span><span class="sxs-lookup"><span data-stu-id="673f1-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="673f1-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="673f1-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673f1-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="673f1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673f1-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="673f1-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
