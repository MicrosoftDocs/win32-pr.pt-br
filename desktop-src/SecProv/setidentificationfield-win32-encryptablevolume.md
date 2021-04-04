---
description: Define a cadeia de caracteres do identificador especificado nos metadados do volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Método setidentificafield da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836975"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6cf62-103">Método setidentificafield da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6cf62-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6cf62-104">O método **Setidentificafield** da classe [**\_ EncryptableVolume do Win32**](win32-encryptablevolume.md) define a cadeia de caracteres do identificador especificado nos metadados do volume.</span><span class="sxs-lookup"><span data-stu-id="6cf62-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cf62-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="6cf62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cf62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf62-107">*Identificação do identificador* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6cf62-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf62-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6cf62-108">Type: **string**</span></span>

<span data-ttu-id="6cf62-109">Uma cadeia de caracteres que especifica o campo de identificação que é atribuído ao volume.</span><span class="sxs-lookup"><span data-stu-id="6cf62-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="6cf62-110">Se a cadeia de caracteres opcional não estiver presente, os valores definidos do registro serão usados.</span><span class="sxs-lookup"><span data-stu-id="6cf62-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="6cf62-111">Se a cadeia de caracteres estiver presente e não estiver vazia, o valor especificado será usado.</span><span class="sxs-lookup"><span data-stu-id="6cf62-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="6cf62-112">O parâmetro *identificafield* não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6cf62-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf62-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cf62-113">Return value</span></span>

<span data-ttu-id="6cf62-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6cf62-114">Type: **uint32**</span></span>

<span data-ttu-id="6cf62-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="6cf62-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6cf62-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6cf62-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6cf62-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cf62-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6cf62-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf62-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6cf62-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6cf62-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="6cf62-120"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf62-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="6cf62-121">Esta unidade está bloqueada por Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6cf62-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="6cf62-122">Você deve desbloquear este volume no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6cf62-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="6cf62-123"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf62-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="6cf62-124">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="6cf62-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6cf62-125">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6cf62-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="6cf62-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cf62-126">Requirements</span></span>



| <span data-ttu-id="6cf62-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf62-127">Requirement</span></span> | <span data-ttu-id="6cf62-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6cf62-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf62-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cf62-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf62-130">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="6cf62-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6cf62-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cf62-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf62-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6cf62-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6cf62-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="6cf62-133">Namespace</span></span><br/>                | <span data-ttu-id="6cf62-134">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6cf62-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6cf62-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6cf62-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cf62-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cf62-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf62-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cf62-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf62-138">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6cf62-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




