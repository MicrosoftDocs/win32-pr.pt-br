---
description: Enumera todos os certificados no sistema que correspondem aos critérios indicados e retorna uma lista de impressões digitais.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Método FindValidCertificates da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297100"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5d071-103">Método FindValidCertificates da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5d071-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5d071-104">O método **FindValidCertificates** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) enumera todos os certificados no sistema que correspondem aos critérios indicados e retorna uma lista de impressões digitais.</span><span class="sxs-lookup"><span data-stu-id="5d071-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="5d071-105">A lista retornada contém apenas certificados com um OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) válido.</span><span class="sxs-lookup"><span data-stu-id="5d071-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="5d071-106">O OID pode ser o padrão ou pode ser especificado no Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="5d071-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d071-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d071-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="5d071-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d071-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d071-109">*CertificateThumbprint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5d071-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d071-110">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d071-110">Type: **string\[\]**</span></span>

<span data-ttu-id="5d071-111">Uma matriz de cadeias de caracteres que contém a lista de certificados válidos.</span><span class="sxs-lookup"><span data-stu-id="5d071-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d071-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d071-112">Return value</span></span>

<span data-ttu-id="5d071-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d071-113">Type: **uint32**</span></span>

<span data-ttu-id="5d071-114">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="5d071-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5d071-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5d071-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="5d071-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d071-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5d071-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5d071-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="5d071-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5d071-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="5d071-119"><dt>**FVE \_ E \_ \_ \_ OID do BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt> inválido</span><span class="sxs-lookup"><span data-stu-id="5d071-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="5d071-120">O OID do BitLocker disponível não é válido.</span><span class="sxs-lookup"><span data-stu-id="5d071-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d071-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d071-121">Requirements</span></span>



| <span data-ttu-id="5d071-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d071-122">Requirement</span></span> | <span data-ttu-id="5d071-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5d071-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d071-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d071-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d071-125">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="5d071-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d071-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d071-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d071-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5d071-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5d071-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d071-128">Namespace</span></span><br/>                | <span data-ttu-id="5d071-129">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5d071-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5d071-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5d071-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d071-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d071-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d071-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d071-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d071-133">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5d071-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
