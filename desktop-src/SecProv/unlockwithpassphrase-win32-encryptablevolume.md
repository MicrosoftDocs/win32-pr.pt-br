---
description: Método UnlockWithPassphrase da classe Win32_EncryptableVolume – usa a frase secreta para obter a chave derivada.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116454"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c8668-103">Método UnlockWithPassphrase da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="c8668-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c8668-104">O método **UnlockWithPassphrase** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a frase secreta para obter a chave derivada.</span><span class="sxs-lookup"><span data-stu-id="c8668-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="c8668-105">Depois que a chave derivada é calculada, a chave derivada é usada para desbloquear a chave mestra do volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="c8668-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="c8668-106">Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="c8668-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c8668-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8668-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="c8668-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8668-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8668-109">*Frase secreta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c8668-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8668-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8668-110">Type: **string**</span></span>

<span data-ttu-id="c8668-111">Uma cadeia de caracteres que especifica a frase secreta.</span><span class="sxs-lookup"><span data-stu-id="c8668-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8668-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c8668-112">Return value</span></span>

<span data-ttu-id="c8668-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8668-113">Type: **uint32**</span></span>

<span data-ttu-id="c8668-114">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="c8668-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c8668-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c8668-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="c8668-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8668-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8668-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="c8668-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c8668-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="c8668-119"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="c8668-120">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="c8668-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c8668-121">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c8668-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="c8668-122"><dt>**FVE \_ E \_ FIPS \_ impede a \_ senha**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="c8668-123">A configuração de política de grupo que requer conformidade com FIPS impediu que a frase secreta fosse gerada ou usada.</span><span class="sxs-lookup"><span data-stu-id="c8668-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="c8668-124"><dt>**FVE \_ E \_ \_ \_ \_ comprimento de senha inválido da política**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="c8668-125">A senha fornecida não atende aos requisitos mínimos ou máximos de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c8668-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="c8668-126"><dt>**FVE \_ Senha da política de E \_ \_ \_ muito \_ simples**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="c8668-127">A senha não atende aos requisitos de complexidade definidos pelo administrador na diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="c8668-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="c8668-128"><dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="c8668-129">O volume não pode ser desbloqueado com as informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="c8668-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="c8668-130"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="c8668-131">O protetor de chave fornecido não existe no volume.</span><span class="sxs-lookup"><span data-stu-id="c8668-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="c8668-132">Você deve inserir outro protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="c8668-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="c8668-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8668-133">Requirements</span></span>



| <span data-ttu-id="c8668-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8668-134">Requirement</span></span> | <span data-ttu-id="c8668-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c8668-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8668-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8668-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c8668-137">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="c8668-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c8668-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8668-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c8668-139">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="c8668-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8668-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8668-140">Namespace</span></span><br/>                | <span data-ttu-id="c8668-141">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c8668-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c8668-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c8668-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8668-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8668-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8668-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c8668-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8668-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c8668-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




