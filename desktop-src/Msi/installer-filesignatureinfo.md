---
description: O método FileSignatureInfo do objeto do instalador usa o caminho para um arquivo e retorna um SAFEARRAY de bytes que representam o hash ou o certificado codificado.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Método Installer. FileSignatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747334"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="5a93c-103">Método Installer. FileSignatureInfo</span><span class="sxs-lookup"><span data-stu-id="5a93c-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="5a93c-104">O método **FileSignatureInfo** do objeto do [**instalador**](installer-object.md) usa o caminho para um arquivo e retorna um SafeArray de bytes que representam o hash ou o certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="5a93c-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="5a93c-105">Os valores podem então ser usados para preencher as tabelas [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5a93c-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="5a93c-106">Para obter mais informações, consulte o [**tipo de dados SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="5a93c-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a93c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a93c-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="5a93c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a93c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a93c-109">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="5a93c-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="5a93c-110">Caminho completo de um arquivo assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="5a93c-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="5a93c-111">Ao preencher as tabelas [MsiDigitalSignature](msidigitalsignature-table.md) e [MsiDigitalCertificate](msidigitalcertificate-table.md) , *FilePath* aponta para um gabinete assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="5a93c-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="5a93c-112">Ao preencher as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate, *FilePath* aponta para um patch assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="5a93c-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="5a93c-113">*Opções*</span><span class="sxs-lookup"><span data-stu-id="5a93c-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="5a93c-114">Sinalizadores de caso de erro especiais.</span><span class="sxs-lookup"><span data-stu-id="5a93c-114">Special error case flags.</span></span>



| <span data-ttu-id="5a93c-115">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="5a93c-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="5a93c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5a93c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="5a93c-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a93c-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="5a93c-118">Com *as opções* definidas como MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** sempre retorna um erro fatal para um hash inválido.</span><span class="sxs-lookup"><span data-stu-id="5a93c-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="5a93c-119">Se *as opções* não estiverem definidas como msiSignatureOptionInvalidHashFatal e o *formato* for definido como msiSignatureInfoCertificate, **FileSignatureInfo** não retornará um erro para um hash inválido.</span><span class="sxs-lookup"><span data-stu-id="5a93c-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a93c-120">*Formato*</span><span class="sxs-lookup"><span data-stu-id="5a93c-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="5a93c-121">As informações de assinatura solicitadas.</span><span class="sxs-lookup"><span data-stu-id="5a93c-121">The requested signature information.</span></span>



| <span data-ttu-id="5a93c-122">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="5a93c-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="5a93c-123">Significado</span><span class="sxs-lookup"><span data-stu-id="5a93c-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="5a93c-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5a93c-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="5a93c-125">Retorna um SAFEARRAY de bytes que representa o certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="5a93c-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="5a93c-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a93c-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="5a93c-127">Retorna um SAFEARRAY de bytes que representa o hash.</span><span class="sxs-lookup"><span data-stu-id="5a93c-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a93c-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a93c-128">Return value</span></span>

<span data-ttu-id="5a93c-129">Se for bem-sucedido, o método retornará um [SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray) de bytes que contenham o certificado hash ou codificado.</span><span class="sxs-lookup"><span data-stu-id="5a93c-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a93c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a93c-130">Remarks</span></span>

<span data-ttu-id="5a93c-131">Para criar uma instalação assinada totalmente verificada usando a automação, use o método **FileSignatureInfo** para popular as tabelas [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalSignature](msidigitalsignature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5a93c-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="5a93c-132">Para obter mais informações, consulte [criando uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="5a93c-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a93c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a93c-133">Requirements</span></span>



| <span data-ttu-id="5a93c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a93c-134">Requirement</span></span> | <span data-ttu-id="5a93c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5a93c-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a93c-136">Versão</span><span class="sxs-lookup"><span data-stu-id="5a93c-136">Version</span></span><br/> | <span data-ttu-id="5a93c-137">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a93c-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5a93c-138">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a93c-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5a93c-139">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a93c-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5a93c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5a93c-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a93c-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a93c-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5a93c-142">IID</span><span class="sxs-lookup"><span data-stu-id="5a93c-142">IID</span></span><br/>     | <span data-ttu-id="5a93c-143">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5a93c-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="5a93c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a93c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a93c-145">Criando uma instalação assinada totalmente verificada usando a automação</span><span class="sxs-lookup"><span data-stu-id="5a93c-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="5a93c-146">Assinaturas digitais e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5a93c-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="5a93c-147">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="5a93c-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
