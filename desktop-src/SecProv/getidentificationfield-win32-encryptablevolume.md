---
description: Retorna a cadeia de caracteres do identificador disponível nos metadados do volume.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Método getidentificafield da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090173"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3f1cf-103">Método getidentificafield da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="3f1cf-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3f1cf-104">O método **Getidentificafield** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retorna a cadeia de caracteres do identificador disponível nos metadados do volume.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f1cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f1cf-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="3f1cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f1cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f1cf-107">*Identificação do identificador* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f1cf-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f1cf-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3f1cf-108">Type: **string**</span></span>

<span data-ttu-id="3f1cf-109">Uma cadeia de caracteres que especifica o campo de identificação que é atribuído ao volume.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f1cf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f1cf-110">Return value</span></span>

<span data-ttu-id="3f1cf-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f1cf-111">Type: **uint32**</span></span>

<span data-ttu-id="3f1cf-112">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3f1cf-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3f1cf-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="3f1cf-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f1cf-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f1cf-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3f1cf-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="3f1cf-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="3f1cf-117"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3f1cf-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="3f1cf-118">Esta unidade está bloqueada por Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="3f1cf-119">Você deve desbloquear este volume no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="3f1cf-120"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3f1cf-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="3f1cf-121">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3f1cf-122">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="3f1cf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f1cf-123">Requirements</span></span>



| <span data-ttu-id="3f1cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f1cf-124">Requirement</span></span> | <span data-ttu-id="3f1cf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3f1cf-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f1cf-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f1cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f1cf-127">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="3f1cf-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f1cf-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f1cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f1cf-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3f1cf-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3f1cf-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f1cf-130">Namespace</span></span><br/>                | <span data-ttu-id="3f1cf-131">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3f1cf-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3f1cf-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3f1cf-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f1cf-133"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f1cf-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f1cf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f1cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1cf-135">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="3f1cf-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




