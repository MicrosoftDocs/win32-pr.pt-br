---
description: Usa a cadeia de caracteres de SID (identificador de segurança) Active Directory fornecida para obter a chave derivada e desbloquear o volume criptografado.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Método UnlockWithAdSid da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754118"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="93f20-103">Método UnlockWithAdSid da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="93f20-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="93f20-104">O método **UnlockWithAdSid** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a cadeia de caracteres de Sid (identificador de segurança) Active Directory fornecida para obter a chave derivada e desbloquear o volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="93f20-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="93f20-105">Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="93f20-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="93f20-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93f20-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="93f20-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93f20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f20-108">*SidString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93f20-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f20-109">Cadeia de caracteres que contém o Active Directory SID.</span><span class="sxs-lookup"><span data-stu-id="93f20-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f20-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93f20-110">Return value</span></span>

<span data-ttu-id="93f20-111">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="93f20-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="93f20-112">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="93f20-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="93f20-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="93f20-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="93f20-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="93f20-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="93f20-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="93f20-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93f20-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="93f20-116">Remarks</span></span>

<span data-ttu-id="93f20-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="93f20-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93f20-118">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="93f20-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="93f20-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="93f20-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93f20-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="93f20-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93f20-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f20-121">Requirements</span></span>



| <span data-ttu-id="93f20-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f20-122">Requirement</span></span> | <span data-ttu-id="93f20-123">Valor</span><span class="sxs-lookup"><span data-stu-id="93f20-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f20-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93f20-124">Minimum supported client</span></span><br/> | <span data-ttu-id="93f20-125">Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]</span><span class="sxs-lookup"><span data-stu-id="93f20-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93f20-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93f20-126">Minimum supported server</span></span><br/> | <span data-ttu-id="93f20-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="93f20-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93f20-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="93f20-128">Namespace</span></span><br/>                | <span data-ttu-id="93f20-129">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="93f20-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="93f20-130">MOF</span><span class="sxs-lookup"><span data-stu-id="93f20-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93f20-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93f20-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f20-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="93f20-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f20-133">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="93f20-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
