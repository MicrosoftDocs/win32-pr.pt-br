---
description: Valida o OID (identificador de objeto) de uso avançado de chave (EKU) do certificado fornecido.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Método ProtectKeyWithCertificateThumbprint da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779340"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d9648-103">Método ProtectKeyWithCertificateThumbprint da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="d9648-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d9648-104">O método **ProtectKeyWithCertificateThumbprint** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) valida o OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) de uso avançado de chave (EKU) do certificado fornecido.</span><span class="sxs-lookup"><span data-stu-id="d9648-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9648-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9648-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="d9648-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9648-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9648-107">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d9648-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d9648-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9648-108">Type: **string**</span></span>

<span data-ttu-id="d9648-109">Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="d9648-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="d9648-110">Se esse parâmetro não for especificado, o parâmetro *FriendlyName* será criado usando o nome da entidade no certificado.</span><span class="sxs-lookup"><span data-stu-id="d9648-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="d9648-111">*CertThumbprint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9648-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9648-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9648-112">Type: **string**</span></span>

<span data-ttu-id="d9648-113">Uma cadeia de caracteres que especifica a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="d9648-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="d9648-114">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d9648-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9648-115">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9648-115">Type: **string**</span></span>

<span data-ttu-id="d9648-116">Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado que pode ser usado para gerenciar esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="d9648-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="d9648-117">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="d9648-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9648-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9648-118">Return value</span></span>

<span data-ttu-id="d9648-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9648-119">Type: **uint32**</span></span>

<span data-ttu-id="d9648-120">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="d9648-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d9648-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d9648-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="d9648-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9648-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9648-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="d9648-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d9648-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d9648-125"><dt>**Erro \_ do \_Dados INválidos**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="d9648-126">Os dados não são válidos.</span><span class="sxs-lookup"><span data-stu-id="d9648-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d9648-127"><dt>**FVE \_ E \_ não é o \_ \_ OID do BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="d9648-128">O atributo EKU do certificado especificado não permite que ele seja usado para Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d9648-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="d9648-129">O BitLocker não exige que um certificado tenha um atributo EKU, mas se um estiver configurado, ele deverá ser definido como um OID que corresponda à OID configurada para o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d9648-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="d9648-130"><dt>**FVE \_ O \_ certificado de usuário de política E \_ não é \_ \_ \_ permitido**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="d9648-131">Política de Grupo não permite que certificados de usuário, como cartões inteligentes, sejam usados com o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d9648-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="d9648-132"><dt>**FVE \_ O \_ certificado do usuário da política E \_ \_ \_ deve \_ ser \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="d9648-133">Política de Grupo exige que você forneça um cartão inteligente para usar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d9648-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="d9648-134"><dt>**FVE \_ A \_ política E \_ proíbe \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="d9648-135">Política de Grupo não permite o uso de certificados autoassinados.</span><span class="sxs-lookup"><span data-stu-id="d9648-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d9648-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9648-136">Remarks</span></span>

<span data-ttu-id="d9648-137">Se o OID não corresponder ao que está associado ao controlador de serviço no registro, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="d9648-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="d9648-138">Isso impede que o usuário configure os protetores do agente de recuperação de dados (DRA) manualmente no volume.</span><span class="sxs-lookup"><span data-stu-id="d9648-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="d9648-139">Os DRAs são apenas para serem definidos pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="d9648-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9648-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9648-140">Requirements</span></span>



| <span data-ttu-id="d9648-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9648-141">Requirement</span></span> | <span data-ttu-id="d9648-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d9648-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9648-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9648-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d9648-144">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="d9648-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d9648-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9648-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d9648-146">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d9648-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d9648-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9648-147">Namespace</span></span><br/>                | <span data-ttu-id="d9648-148">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d9648-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d9648-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d9648-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9648-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9648-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9648-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9648-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9648-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="d9648-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
