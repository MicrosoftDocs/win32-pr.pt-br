---
description: Método ProtectKeyWithCertificateFile da classe Win32_EncryptableVolume – valida o OID (identificador de objeto) de uso avançado de chave (EKU) do certificado fornecido.
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Método ProtectKeyWithCertificateFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110555"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6d35d-103">Método ProtectKeyWithCertificateFile da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6d35d-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6d35d-104">O método **ProtectKeyWithCertificateFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) valida o OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) de uso avançado de chave (EKU) do certificado fornecido.</span><span class="sxs-lookup"><span data-stu-id="6d35d-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d35d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d35d-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6d35d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d35d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d35d-107">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6d35d-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d35d-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d35d-108">Type: **string**</span></span>

<span data-ttu-id="6d35d-109">Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="6d35d-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="6d35d-110">Se esse parâmetro não for especificado, o parâmetro *FriendlyName* será criado usando o nome da entidade no certificado.</span><span class="sxs-lookup"><span data-stu-id="6d35d-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6d35d-111">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d35d-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d35d-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d35d-112">Type: **string**</span></span>

<span data-ttu-id="6d35d-113">Uma cadeia de caracteres que especifica o local e o nome do arquivo. cer usado para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6d35d-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="6d35d-114">Um certificado de criptografia deve ser exportado no formato. cer ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) – binário codificado [*x. 509*](../secgloss/x-gly.md) ou x. 509 codificado em base-64).</span><span class="sxs-lookup"><span data-stu-id="6d35d-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="6d35d-115">O certificado de criptografia pode ser gerado por meio da PKI da Microsoft, PKI de terceiros ou autoassinado.</span><span class="sxs-lookup"><span data-stu-id="6d35d-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="6d35d-116">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6d35d-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d35d-117">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d35d-117">Type: **string**</span></span>

<span data-ttu-id="6d35d-118">Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado que pode ser usado para gerenciar esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="6d35d-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="6d35d-119">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="6d35d-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d35d-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6d35d-120">Return value</span></span>

<span data-ttu-id="6d35d-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d35d-121">Type: **uint32**</span></span>

<span data-ttu-id="6d35d-122">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="6d35d-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6d35d-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6d35d-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="6d35d-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d35d-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d35d-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="6d35d-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6d35d-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="6d35d-127"><dt>**FVE \_ E \_ não é o \_ \_ OID do BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="6d35d-128">O atributo EKU do certificado especificado não permite que ele seja usado para Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6d35d-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="6d35d-129">O BitLocker não exige que um certificado tenha um atributo EKU, mas se um estiver configurado, ele deverá ser definido como um OID que corresponda à OID configurada para o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6d35d-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="6d35d-130"><dt>**FVE \_ O \_ certificado de usuário de política E \_ não é \_ \_ \_ permitido**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="6d35d-131">Política de Grupo não permite que certificados de usuário, como cartões inteligentes, sejam usados com o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6d35d-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="6d35d-132"><dt>**FVE \_ O \_ certificado do usuário da política E \_ \_ \_ deve \_ ser \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="6d35d-133">Política de Grupo exige que você forneça um cartão inteligente para usar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6d35d-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="6d35d-134"><dt>**FVE \_ A \_ política E \_ proíbe \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="6d35d-135">Política de Grupo não permite o uso de certificados autoassinados.</span><span class="sxs-lookup"><span data-stu-id="6d35d-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="6d35d-136"><dt>**Erro \_ do ARQUIVO \_ não \_ encontrado**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="6d35d-137">O sistema não pode localizar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6d35d-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="6d35d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d35d-138">Remarks</span></span>

<span data-ttu-id="6d35d-139">Se o OID não corresponder ao que está associado ao controlador de serviço no registro, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="6d35d-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="6d35d-140">Isso impede que o usuário configure os protetores do agente de recuperação de dados (DRA) manualmente no volume.</span><span class="sxs-lookup"><span data-stu-id="6d35d-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="6d35d-141">Os DRAs são apenas para serem definidos pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="6d35d-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d35d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d35d-142">Requirements</span></span>



| <span data-ttu-id="6d35d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d35d-143">Requirement</span></span> | <span data-ttu-id="6d35d-144">Valor</span><span class="sxs-lookup"><span data-stu-id="6d35d-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d35d-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d35d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6d35d-146">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="6d35d-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d35d-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d35d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6d35d-148">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6d35d-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6d35d-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d35d-149">Namespace</span></span><br/>                | <span data-ttu-id="6d35d-150">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6d35d-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6d35d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="6d35d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d35d-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d35d-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d35d-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6d35d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d35d-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6d35d-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
