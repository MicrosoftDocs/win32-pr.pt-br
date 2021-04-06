---
description: Usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Método UnlockWithNumericalPassword da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826967"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9abdd-103">Método UnlockWithNumericalPassword da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="9abdd-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9abdd-104">O método **UnlockWithNumericalPassword** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.</span><span class="sxs-lookup"><span data-stu-id="9abdd-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="9abdd-105">A chave de criptografia do volume deve ter sido protegida com um ou mais protetores de chave do tipo "senha numérica" (usando o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) para poder desbloquear o volume com esse método.</span><span class="sxs-lookup"><span data-stu-id="9abdd-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="9abdd-106">Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="9abdd-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9abdd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9abdd-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="9abdd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9abdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9abdd-109">*NumericalPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9abdd-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9abdd-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9abdd-110">Type: **string**</span></span>

<span data-ttu-id="9abdd-111">Uma cadeia de caracteres que especifica a senha numérica.</span><span class="sxs-lookup"><span data-stu-id="9abdd-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="9abdd-112">A senha numérica deve conter 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="9abdd-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="9abdd-113">Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo, indicando um valor de soma de verificação para o grupo.</span><span class="sxs-lookup"><span data-stu-id="9abdd-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="9abdd-114">Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 65536.</span><span class="sxs-lookup"><span data-stu-id="9abdd-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="9abdd-115">Supondo que um grupo de seis dígitos seja rotulado como X1, X2, X3, x4, X5 e X6, o dígito de soma de verificação X6 é calculado como – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="9abdd-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="9abdd-116">Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen.</span><span class="sxs-lookup"><span data-stu-id="9abdd-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="9abdd-117">Portanto, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" ou "XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX, XXXXXX XXXXXX", também pode conter senhas numéricas válidas.</span><span class="sxs-lookup"><span data-stu-id="9abdd-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9abdd-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9abdd-118">Return value</span></span>

<span data-ttu-id="9abdd-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9abdd-119">Type: **uint32**</span></span>

<span data-ttu-id="9abdd-120">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="9abdd-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="9abdd-121">Se o volume já estiver desbloqueado e nenhum outro erro ocorrer, esse método retornará 0.</span><span class="sxs-lookup"><span data-stu-id="9abdd-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="9abdd-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9abdd-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="9abdd-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="9abdd-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9abdd-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9abdd-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="9abdd-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9abdd-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="9abdd-126"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9abdd-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="9abdd-127">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="9abdd-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9abdd-128">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9abdd-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="9abdd-129"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="9abdd-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="9abdd-130">O volume não tem um protetor de chave do tipo "senha numérica".</span><span class="sxs-lookup"><span data-stu-id="9abdd-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="9abdd-131">O parâmetro *NumericalPassword* tem um formato válido, mas você não pode usar uma senha numérica para desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="9abdd-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="9abdd-132"><dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="9abdd-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="9abdd-133">O parâmetro *NumericalPassword* não pode desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="9abdd-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="9abdd-134">Existe um ou mais protetores de chave do tipo "senha numérica", mas o parâmetro *NumericalPassword* especificado não pode desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="9abdd-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="9abdd-135"><dt>**FVE \_ E \_ \_ \_ formato de senha inválido**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="9abdd-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="9abdd-136">O parâmetro *NumericalPassword* não tem um formato válido.</span><span class="sxs-lookup"><span data-stu-id="9abdd-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="9abdd-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="9abdd-137">Remarks</span></span>

<span data-ttu-id="9abdd-138">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9abdd-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9abdd-139">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9abdd-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9abdd-140">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9abdd-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9abdd-141">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9abdd-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9abdd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9abdd-142">Requirements</span></span>



| <span data-ttu-id="9abdd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9abdd-143">Requirement</span></span> | <span data-ttu-id="9abdd-144">Valor</span><span class="sxs-lookup"><span data-stu-id="9abdd-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9abdd-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9abdd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9abdd-146">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="9abdd-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9abdd-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9abdd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9abdd-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9abdd-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9abdd-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="9abdd-149">Namespace</span></span><br/>                | <span data-ttu-id="9abdd-150">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9abdd-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9abdd-151">MOF</span><span class="sxs-lookup"><span data-stu-id="9abdd-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9abdd-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9abdd-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abdd-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9abdd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abdd-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="9abdd-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
