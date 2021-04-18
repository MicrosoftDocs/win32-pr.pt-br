---
description: Copia o conteúdo de um repositório de certificados aberto para uma cadeia de caracteres codificada.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Método Store. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753212"
---
# <a name="storeexport-method"></a><span data-ttu-id="cb031-103">Método Store. Export</span><span class="sxs-lookup"><span data-stu-id="cb031-103">Store.Export method</span></span>

<span data-ttu-id="cb031-104">\[O método de **exportação** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="cb031-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb031-105">Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cb031-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cb031-106">O método de **exportação** copia o conteúdo de um [*repositório de certificados*](../secgloss/c-gly.md) aberto para uma cadeia de caracteres codificada.</span><span class="sxs-lookup"><span data-stu-id="cb031-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb031-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb031-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cb031-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb031-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb031-109">*Salvar como* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cb031-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb031-110">Um valor da enumeração [de \_ \_ tipo salvar \_ como \_ do armazenamento capicor](capicom-store-save-as-type.md) que indica o formato da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="cb031-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="cb031-111">O valor padrão é capicote \_ Store \_ Save \_ as \_ serializado.</span><span class="sxs-lookup"><span data-stu-id="cb031-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="cb031-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cb031-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="cb031-113">Valor</span><span class="sxs-lookup"><span data-stu-id="cb031-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="cb031-114">Significado</span><span class="sxs-lookup"><span data-stu-id="cb031-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="cb031-115"><dt>**capicote \_ Store \_ Save \_ as \_ serializado**</dt></span><span class="sxs-lookup"><span data-stu-id="cb031-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="cb031-116">O repositório é salvo no formato serializado.</span><span class="sxs-lookup"><span data-stu-id="cb031-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="cb031-117"><dt>**Capicote \_ Store \_ Save \_ as \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="cb031-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="cb031-118">O repositório é salvo no \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="cb031-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="cb031-119">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cb031-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb031-120">Um valor da enumeração [do \_ \_ tipo de codificação capicor](capicom-encoding-type.md) que indica o tipo de codificação do repositório exportado.</span><span class="sxs-lookup"><span data-stu-id="cb031-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="cb031-121">O valor padrão é CAPICOM de \_ codificação \_ base64.</span><span class="sxs-lookup"><span data-stu-id="cb031-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="cb031-122">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cb031-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="cb031-123">Valor</span><span class="sxs-lookup"><span data-stu-id="cb031-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="cb031-124">Significado</span><span class="sxs-lookup"><span data-stu-id="cb031-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="cb031-125"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="cb031-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="cb031-126">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="cb031-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="cb031-127">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="cb031-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="cb031-128">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cb031-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="cb031-129"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="cb031-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="cb031-130">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="cb031-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="cb031-131"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="cb031-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="cb031-132">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="cb031-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb031-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb031-133">Return value</span></span>

<span data-ttu-id="cb031-134">Esse método retorna uma cadeia de caracteres que contém os certificados no repositório no formulário de codificação especificado.</span><span class="sxs-lookup"><span data-stu-id="cb031-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb031-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb031-135">Requirements</span></span>



| <span data-ttu-id="cb031-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb031-136">Requirement</span></span> | <span data-ttu-id="cb031-137">Valor</span><span class="sxs-lookup"><span data-stu-id="cb031-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb031-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="cb031-138">Redistributable</span></span><br/> | <span data-ttu-id="cb031-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb031-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cb031-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cb031-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="cb031-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb031-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb031-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb031-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb031-143">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="cb031-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="cb031-144">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="cb031-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
