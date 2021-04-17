---
description: Usa o arquivo de certificado fornecido para obter a chave derivada e desbloquear o volume criptografado.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Método UnlockWithCertificateFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754119"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="faf60-103">Método UnlockWithCertificateFile da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="faf60-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="faf60-104">O método **UnlockWithCertificateFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa o arquivo de [*certificado*](../secgloss/c-gly.md) fornecido para obter a chave derivada e desbloquear o volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="faf60-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="faf60-105">Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="faf60-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="faf60-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faf60-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="faf60-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faf60-108">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="faf60-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf60-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="faf60-109">Type: **string**</span></span>

<span data-ttu-id="faf60-110">Uma cadeia de caracteres que especifica o local e o nome do arquivo. cer usado para recuperar a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="faf60-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="faf60-111">Um certificado de [*criptografia*](../secgloss/e-gly.md) deve ser exportado no formato. cer ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) – binário codificado [*x. 509*](../secgloss/x-gly.md) ou x. 509 codificado em base-64).</span><span class="sxs-lookup"><span data-stu-id="faf60-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="faf60-112">O certificado de criptografia pode ser gerado por meio da PKI da Microsoft, PKI de terceiros ou autoassinado.</span><span class="sxs-lookup"><span data-stu-id="faf60-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="faf60-113">*Fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="faf60-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf60-114">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="faf60-114">Type: **string**</span></span>

<span data-ttu-id="faf60-115">Uma cadeia de caracteres de identificação pessoal especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="faf60-115">A user-specified personal identification string.</span></span> <span data-ttu-id="faf60-116">Essa cadeia de caracteres deve consistir em uma sequência de 4 a 20 dígitos.</span><span class="sxs-lookup"><span data-stu-id="faf60-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="faf60-117">Essa cadeia de caracteres é usada para autenticar silenciosamente o KSP ( [*provedor de armazenamento de chaves*](../secgloss/k-gly.md) ) quando usado com um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="faf60-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf60-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="faf60-118">Return value</span></span>

<span data-ttu-id="faf60-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="faf60-119">Type: **uint32**</span></span>

<span data-ttu-id="faf60-120">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="faf60-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="faf60-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="faf60-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="faf60-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="faf60-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faf60-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="faf60-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="faf60-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="faf60-125"><dt>**Erro \_ do ARQUIVO \_ não \_ encontrado**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="faf60-126">O sistema não pode arquivar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="faf60-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="faf60-127"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="faf60-128">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="faf60-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="faf60-129">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="faf60-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="faf60-130"><dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="faf60-131">O volume não pode ser desbloqueado com as informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="faf60-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="faf60-132"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="faf60-133">O protetor de chave fornecido não existe no volume.</span><span class="sxs-lookup"><span data-stu-id="faf60-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="faf60-134">Você deve inserir outro protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="faf60-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="faf60-135"><dt>**FVE \_ \_Falha de \_ autenticação \_ do E PRIVATEKEY**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="faf60-136">A [*chave privada*](../secgloss/p-gly.md), associada ao certificado especificado, não pôde ser autorizada.</span><span class="sxs-lookup"><span data-stu-id="faf60-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="faf60-137">A autorização de chave privada não foi fornecida ou a autorização fornecida era inválida.</span><span class="sxs-lookup"><span data-stu-id="faf60-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="faf60-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf60-138">Requirements</span></span>



| <span data-ttu-id="faf60-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="faf60-139">Requirement</span></span> | <span data-ttu-id="faf60-140">Valor</span><span class="sxs-lookup"><span data-stu-id="faf60-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf60-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faf60-141">Minimum supported client</span></span><br/> | <span data-ttu-id="faf60-142">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="faf60-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="faf60-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faf60-143">Minimum supported server</span></span><br/> | <span data-ttu-id="faf60-144">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="faf60-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="faf60-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="faf60-145">Namespace</span></span><br/>                | <span data-ttu-id="faf60-146">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="faf60-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="faf60-147">MOF</span><span class="sxs-lookup"><span data-stu-id="faf60-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faf60-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faf60-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf60-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="faf60-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf60-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="faf60-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
