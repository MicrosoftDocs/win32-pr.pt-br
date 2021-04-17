---
description: Recupera o nome de exibição usado para identificar um protetor de chave específico.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Método GetKeyProtectorFriendlyName da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782937"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="dc868-103">Método GetKeyProtectorFriendlyName da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="dc868-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="dc868-104">O método **GetKeyProtectorFriendlyName** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera o nome de exibição usado para identificar um protetor de chave específico.</span><span class="sxs-lookup"><span data-stu-id="dc868-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc868-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc868-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="dc868-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc868-107">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dc868-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc868-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dc868-108">Type: **string**</span></span>

<span data-ttu-id="dc868-109">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="dc868-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="dc868-110">*FriendlyName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc868-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc868-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dc868-111">Type: **string**</span></span>

<span data-ttu-id="dc868-112">Uma cadeia de caracteres que contém o nome especificado pelo usuário usado para identificar o protetor de chave fornecido.</span><span class="sxs-lookup"><span data-stu-id="dc868-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc868-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc868-113">Return value</span></span>

<span data-ttu-id="dc868-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc868-114">Type: **uint32**</span></span>

<span data-ttu-id="dc868-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="dc868-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="dc868-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dc868-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="dc868-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc868-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc868-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dc868-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="dc868-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dc868-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dc868-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="dc868-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="dc868-121">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave válido.</span><span class="sxs-lookup"><span data-stu-id="dc868-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="dc868-122"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="dc868-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="dc868-123">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="dc868-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="dc868-124">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dc868-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc868-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc868-125">Remarks</span></span>

<span data-ttu-id="dc868-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dc868-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dc868-127">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc868-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dc868-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="dc868-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dc868-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dc868-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc868-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc868-130">Requirements</span></span>



| <span data-ttu-id="dc868-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc868-131">Requirement</span></span> | <span data-ttu-id="dc868-132">Valor</span><span class="sxs-lookup"><span data-stu-id="dc868-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc868-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc868-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dc868-134">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="dc868-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dc868-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc868-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dc868-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc868-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc868-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc868-137">Namespace</span></span><br/>                | <span data-ttu-id="dc868-138">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="dc868-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="dc868-139">MOF</span><span class="sxs-lookup"><span data-stu-id="dc868-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc868-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc868-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc868-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc868-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc868-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="dc868-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
