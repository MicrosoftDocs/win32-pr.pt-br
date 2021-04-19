---
description: Copia um certificado para uma cadeia de caracteres codificada.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'Método ICertificate2:: Export'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756686"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="25758-103">Método ICertificate2:: Export</span><span class="sxs-lookup"><span data-stu-id="25758-103">ICertificate2::Export method</span></span>

<span data-ttu-id="25758-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25758-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="25758-105">Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="25758-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="25758-106">O método **Export** copia um certificado para uma cadeia de caracteres codificada.</span><span class="sxs-lookup"><span data-stu-id="25758-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="25758-107">A cadeia de caracteres codificada pode ser gravada em um arquivo ou importada para um novo objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="25758-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25758-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25758-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="25758-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25758-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25758-110">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="25758-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25758-111">Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que especifica o tipo de codificação para a operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="25758-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="25758-112">O valor padrão é **CAPICOM de \_ codificação \_ Base64**.</span><span class="sxs-lookup"><span data-stu-id="25758-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="25758-113">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="25758-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="25758-114">Valor</span><span class="sxs-lookup"><span data-stu-id="25758-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="25758-115">Significado</span><span class="sxs-lookup"><span data-stu-id="25758-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="25758-116"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="25758-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="25758-117">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="25758-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="25758-118">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="25758-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="25758-119">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="25758-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="25758-120"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="25758-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="25758-121">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="25758-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="25758-122"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="25758-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="25758-123">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="25758-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25758-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25758-124">Return value</span></span>

<span data-ttu-id="25758-125">Uma cadeia de caracteres que contém o certificado exportado no formulário de codificação especificado.</span><span class="sxs-lookup"><span data-stu-id="25758-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="25758-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25758-126">Requirements</span></span>



| <span data-ttu-id="25758-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="25758-127">Requirement</span></span> | <span data-ttu-id="25758-128">Valor</span><span class="sxs-lookup"><span data-stu-id="25758-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25758-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="25758-129">End of client support</span></span><br/> | <span data-ttu-id="25758-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25758-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="25758-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="25758-131">End of server support</span></span><br/> | <span data-ttu-id="25758-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25758-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="25758-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="25758-133">Redistributable</span></span><br/>       | <span data-ttu-id="25758-134">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="25758-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="25758-135">DLL</span><span class="sxs-lookup"><span data-stu-id="25758-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="25758-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25758-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25758-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="25758-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25758-138">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="25758-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="25758-139">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="25758-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
