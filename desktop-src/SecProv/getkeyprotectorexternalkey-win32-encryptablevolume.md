---
description: Recupera a chave externa para um determinado protetor de chave.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Método GetKeyProtectorExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164392"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="13182-103">Método GetKeyProtectorExternalKey da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="13182-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="13182-104">O método **GetKeyProtectorExternalKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera a chave externa para um determinado protetor de chave do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="13182-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="13182-105">O identificador de protetor de chave deve se referir a um protetor de chave do tipo "chave externa", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="13182-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="13182-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13182-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="13182-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13182-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13182-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13182-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13182-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13182-109">Type: **string**</span></span>

<span data-ttu-id="13182-110">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="13182-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="13182-111">*ExternalKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="13182-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13182-112">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="13182-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="13182-113">Uma matriz de bytes que especifica a chave externa de 256 bits que pode ser usada para desbloquear o volume correspondente.</span><span class="sxs-lookup"><span data-stu-id="13182-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13182-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13182-114">Return value</span></span>

<span data-ttu-id="13182-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13182-115">Type: **uint32**</span></span>

<span data-ttu-id="13182-116">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="13182-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="13182-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13182-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="13182-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="13182-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13182-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="13182-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="13182-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="13182-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="13182-121"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="13182-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="13182-122">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="13182-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="13182-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="13182-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="13182-124">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "chave externa", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="13182-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="13182-125"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="13182-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="13182-126">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="13182-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="13182-127">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13182-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="13182-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="13182-128">Remarks</span></span>

<span data-ttu-id="13182-129">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="13182-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="13182-130">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="13182-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="13182-131">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="13182-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="13182-132">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="13182-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13182-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13182-133">Requirements</span></span>



| <span data-ttu-id="13182-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="13182-134">Requirement</span></span> | <span data-ttu-id="13182-135">Valor</span><span class="sxs-lookup"><span data-stu-id="13182-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13182-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13182-136">Minimum supported client</span></span><br/> | <span data-ttu-id="13182-137">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="13182-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13182-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13182-138">Minimum supported server</span></span><br/> | <span data-ttu-id="13182-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13182-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13182-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="13182-140">Namespace</span></span><br/>                | <span data-ttu-id="13182-141">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="13182-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="13182-142">MOF</span><span class="sxs-lookup"><span data-stu-id="13182-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13182-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13182-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13182-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="13182-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13182-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="13182-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
