---
description: Usa a nova senha para obter uma nova chave derivada.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Método ChangePassphrase da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780155"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6bb79-103">Método ChangePassphrase da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6bb79-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6bb79-104">O método **ChangePassphrase** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a nova senha para obter uma nova chave derivada.</span><span class="sxs-lookup"><span data-stu-id="6bb79-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="6bb79-105">Depois que a chave derivada é calculada, a nova chave derivada é usada para proteger a chave mestra do volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="6bb79-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb79-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bb79-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6bb79-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bb79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb79-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb79-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb79-109">Type: **string**</span></span>

<span data-ttu-id="6bb79-110">Um identificador de cadeia de caracteres exclusivo que é usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="6bb79-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="6bb79-111">*NewPassphrase* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb79-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb79-112">Type: **string**</span></span>

<span data-ttu-id="6bb79-113">Uma cadeia de caracteres atualizada que especifica a frase secreta.</span><span class="sxs-lookup"><span data-stu-id="6bb79-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="6bb79-114">*NewProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb79-115">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb79-115">Type: **string**</span></span>

<span data-ttu-id="6bb79-116">Um identificador de cadeia de caracteres exclusivo atualizado usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="6bb79-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb79-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bb79-117">Return value</span></span>

<span data-ttu-id="6bb79-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6bb79-118">Type: **uint32**</span></span>

<span data-ttu-id="6bb79-119">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="6bb79-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6bb79-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6bb79-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="6bb79-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bb79-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6bb79-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="6bb79-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6bb79-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="6bb79-124"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="6bb79-125">O volume já está bloqueado por Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6bb79-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="6bb79-126">Você deve desbloquear a unidade no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6bb79-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="6bb79-127"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="6bb79-128">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="6bb79-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6bb79-129">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6bb79-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="6bb79-130"><dt>**FVE \_ \_ \_ Atualização do E Overlapped**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="6bb79-131">O bloco de controle do volume criptografado foi atualizado por outro thread.</span><span class="sxs-lookup"><span data-stu-id="6bb79-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6bb79-132"><dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="6bb79-133">O protetor de chave especificado não é do tipo correto.</span><span class="sxs-lookup"><span data-stu-id="6bb79-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="6bb79-134"><dt>**FVE \_ E \_ \_ \_ \_ comprimento de senha inválido da política**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="6bb79-135">A senha atualizada fornecida não atende aos requisitos mínimos ou máximos de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6bb79-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="6bb79-136"><dt>**FVE \_ Senha da política de E \_ \_ \_ muito \_ simples**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="6bb79-137">A senha atualizada não atende aos requisitos de complexidade definidos pelo administrador na diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="6bb79-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="6bb79-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bb79-138">Requirements</span></span>



| <span data-ttu-id="6bb79-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb79-139">Requirement</span></span> | <span data-ttu-id="6bb79-140">Valor</span><span class="sxs-lookup"><span data-stu-id="6bb79-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb79-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bb79-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb79-142">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6bb79-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bb79-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb79-144">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6bb79-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="6bb79-145">Namespace</span></span><br/>                | <span data-ttu-id="6bb79-146">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6bb79-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6bb79-147">MOF</span><span class="sxs-lookup"><span data-stu-id="6bb79-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bb79-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bb79-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb79-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bb79-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb79-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6bb79-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




