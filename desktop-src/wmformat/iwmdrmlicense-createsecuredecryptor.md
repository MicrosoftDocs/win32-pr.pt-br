---
title: Método IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: O método CreateSecureDecryptor cria um objeto de descriptografia seguro. O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o novamente de acordo com as configurações especificadas nos parâmetros desse método.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Formato de mídia do Windows do método CreateSecureDecryptor
- Método CreateSecureDecryptor Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762410"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="d1881-107">Método IWMDRMLicense:: CreateSecureDecryptor</span><span class="sxs-lookup"><span data-stu-id="d1881-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="d1881-108">O método **CreateSecureDecryptor** cria um objeto de descriptografia seguro.</span><span class="sxs-lookup"><span data-stu-id="d1881-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="d1881-109">O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o novamente de acordo com as configurações especificadas nos parâmetros desse método.</span><span class="sxs-lookup"><span data-stu-id="d1881-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1881-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1881-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="d1881-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1881-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1881-112">*pbCertificate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1881-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-113">Certificado do aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="d1881-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="d1881-114">*cbCertificate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1881-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-115">Tamanho do certificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="d1881-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d1881-116">*dwCertificateType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1881-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-117">O tipo de certificado.</span><span class="sxs-lookup"><span data-stu-id="d1881-117">The type of the certificate.</span></span> <span data-ttu-id="d1881-118">Defina como \_ XML do tipo de certificado WMDRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d1881-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="d1881-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1881-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-120">O tipo de proteção de sessão a ser usado para nova codificação.</span><span class="sxs-lookup"><span data-stu-id="d1881-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="d1881-121">Deve ser definido como uma das constantes na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1881-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="d1881-122">Constante</span><span class="sxs-lookup"><span data-stu-id="d1881-122">Constant</span></span>                     | <span data-ttu-id="d1881-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1881-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1881-124">\_Tipo de proteção WMDRM \_ \_ RC4</span><span class="sxs-lookup"><span data-stu-id="d1881-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="d1881-125">Usa a criptografia RC4 para criptografia de sessão.</span><span class="sxs-lookup"><span data-stu-id="d1881-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="d1881-126">Esta é a única proteção de sessão com suporte para esta versão.</span><span class="sxs-lookup"><span data-stu-id="d1881-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d1881-127">*pbInitializationVector* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d1881-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-128">Recebe o vetor de inicialização.</span><span class="sxs-lookup"><span data-stu-id="d1881-128">Receives the initialization vector.</span></span> <span data-ttu-id="d1881-129">O vetor de inicialização é o RSA Encrypted usando o esquema de preenchimento OAEP com a chave pública RSA encontrada no certificado.</span><span class="sxs-lookup"><span data-stu-id="d1881-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="d1881-130">Defina como **NULL** para receber o tamanho de buffer necessário em *pcbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="d1881-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="d1881-131">*pcbInitializationVector* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1881-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-132">Na entrada, o tamanho do buffer passado como *pbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="d1881-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="d1881-133">Na saída, o tamanho da parte usada do buffer.</span><span class="sxs-lookup"><span data-stu-id="d1881-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="d1881-134">Se você passar **NULL** para *pbInitializationVector*, esse valor será definido como o tamanho de buffer necessário na saída.</span><span class="sxs-lookup"><span data-stu-id="d1881-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="d1881-135">*ppDecryptor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d1881-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1881-136">Recebe um ponteiro para a interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto recém-criado.</span><span class="sxs-lookup"><span data-stu-id="d1881-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1881-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1881-137">Return value</span></span>

<span data-ttu-id="d1881-138">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d1881-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d1881-139">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1881-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d1881-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d1881-140">Return code</span></span>                                                                          | <span data-ttu-id="d1881-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1881-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d1881-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1881-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d1881-143">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d1881-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1881-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1881-144">Remarks</span></span>

<span data-ttu-id="d1881-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d1881-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1881-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1881-146">Requirements</span></span>



| <span data-ttu-id="d1881-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1881-147">Requirement</span></span> | <span data-ttu-id="d1881-148">Valor</span><span class="sxs-lookup"><span data-stu-id="d1881-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1881-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1881-149">Header</span></span><br/> | <dl> <span data-ttu-id="d1881-150"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1881-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1881-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1881-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1881-152">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="d1881-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





