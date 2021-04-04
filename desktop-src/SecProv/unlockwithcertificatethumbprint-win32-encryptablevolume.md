---
description: Usa a impressão digital do certificado fornecida para obter a chave derivada e desbloquear o volume criptografado.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Método UnlockWithCertificateThumbprint da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646981"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d7fc6-103">Método UnlockWithCertificateThumbprint da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="d7fc6-103">UnlockWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d7fc6-104">O método **UnlockWithCertificateThumbprint** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a impressão digital do [*certificado*](../secgloss/c-gly.md) fornecida para obter a chave derivada e desbloquear o volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-104">The **UnlockWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) thumbprint to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="d7fc6-105">Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="d7fc6-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d7fc6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7fc6-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="d7fc6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7fc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7fc6-108">*CertThumbprint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7fc6-108">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fc6-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7fc6-109">Type: **string**</span></span>

<span data-ttu-id="d7fc6-110">Um valor de impressão digital 0 é aceito e resulta em uma pesquisa do repositório local para o certificado apropriado.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-110">A thumbprint value of 0 is accepted and results in a search of the local store for the appropriate certificate.</span></span> <span data-ttu-id="d7fc6-111">Se um único certificado do BitLocker for encontrado, a pesquisa será bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-111">If a single BitLocker certificate is found, the search is successful.</span></span> <span data-ttu-id="d7fc6-112">Se nenhum ou mais de um certificado for encontrado, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-112">If none or more than one certificate is found, the method fails.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc6-113">*Fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7fc6-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fc6-114">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7fc6-114">Type: **string**</span></span>

<span data-ttu-id="d7fc6-115">Uma cadeia de caracteres de identificação pessoal especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-115">A user-specified personal identification string.</span></span> <span data-ttu-id="d7fc6-116">Essa cadeia de caracteres deve consistir em uma sequência de 4 a 20 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="d7fc6-117">Essa cadeia de caracteres é usada para autenticar silenciosamente o KSP ( [*provedor de armazenamento de chaves*](../secgloss/k-gly.md) ) quando usado com um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d7fc6-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7fc6-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7fc6-118">Return value</span></span>

<span data-ttu-id="d7fc6-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d7fc6-119">Type: **uint32**</span></span>

<span data-ttu-id="d7fc6-120">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d7fc6-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d7fc6-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="d7fc6-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7fc6-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7fc6-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fc6-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="d7fc6-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="d7fc6-125"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fc6-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="d7fc6-126">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="d7fc6-127">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="d7fc6-128"><dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fc6-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="d7fc6-129">O volume não pode ser desbloqueado usando as informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-129">The volume cannot be unlocked by using the provided information.</span></span> <br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="d7fc6-130"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fc6-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="d7fc6-131">O protetor de chave fornecido não existe no volume.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="d7fc6-132">Você deve inserir outro protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-132">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="d7fc6-133"><dt>**FVE \_ \_Falha de \_ autenticação \_ do E PRIVATEKEY**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fc6-133"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="d7fc6-134">Não foi possível autorizar a [*chave privada*](../secgloss/p-gly.md) associada ao certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-134">The [*private key*](../secgloss/p-gly.md) associated with the specified certificate could not be authorized.</span></span> <span data-ttu-id="d7fc6-135">A autorização de chave privada não foi fornecida ou a autorização fornecida não era válida.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-135">The private key authorization was either not provided or the provided authorization was not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7fc6-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7fc6-136">Requirements</span></span>



| <span data-ttu-id="d7fc6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fc6-137">Requirement</span></span> | <span data-ttu-id="d7fc6-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d7fc6-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fc6-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7fc6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fc6-140">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="d7fc6-140">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d7fc6-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7fc6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fc6-142">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d7fc6-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7fc6-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7fc6-143">Namespace</span></span><br/>                | <span data-ttu-id="d7fc6-144">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d7fc6-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d7fc6-145">MOF</span><span class="sxs-lookup"><span data-stu-id="d7fc6-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7fc6-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7fc6-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fc6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7fc6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fc6-148">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="d7fc6-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
