---
description: Especifica o esquema de proteção para exemplos criptografados.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: Atributo MFSampleExtension_Encryption_ProtectionScheme (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091357"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="d6443-103">Atributo MFSampleExtension de \_ criptografia \_ ProtectionScheme</span><span class="sxs-lookup"><span data-stu-id="d6443-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="d6443-104">Especifica o esquema de proteção para exemplos criptografados.</span><span class="sxs-lookup"><span data-stu-id="d6443-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6443-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d6443-105">Data type</span></span>

<span data-ttu-id="d6443-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d6443-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6443-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6443-107">Remarks</span></span>

<span data-ttu-id="d6443-108">O valor desse atributo é um membro da enumeração [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) .</span><span class="sxs-lookup"><span data-stu-id="d6443-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="d6443-109">Nos casos em que a origem da mídia é baseada em MP4, o valor é definido com base no valor do campo **\_ tipo de esquema** na caixa tipo de esquema (' schm ') no cabeçalho MP4 (' Moov ' ou ' Moof ').</span><span class="sxs-lookup"><span data-stu-id="d6443-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="d6443-110">Se o **campo \_ tipo de esquema** em um arquivo baseado em MP4, ou fluxo, for definido como ' Cenc ' ou ' cbc1 ', o **atributo \_ \_ ProtectionScheme de criptografia MFSampleExtension** deverá ser definido como **esquema de proteção \_ \_ AES \_ CTR** ou o **esquema de proteção \_ \_ CBC**, respectivamente, e nenhum valor deve ser definido para MFSampleExtension [ \_ Encryption \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock e [MFSampleExtension \_ Encryption \_](mfsampleextension-encryption-skipbyteblock.md)SkipByteBlock.</span><span class="sxs-lookup"><span data-stu-id="d6443-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="d6443-111">Se o **campo \_ tipo de esquema** em um arquivo baseado em MP4, ou fluxo, for definido como ' Cens ' ou ' CBCs ', o **atributo \_ \_ ProtectionScheme de criptografia MFSampleExtension** deverá ser definido como **esquema de proteção \_ \_ AES \_ CTR** ou o **esquema de proteção \_ \_ CBC**, respectivamente, e MFSampleExtension [ \_ criptografia \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock e MFSampleExtension [ \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) devem ser definidos usando os valores na caixa ' tenc '.</span><span class="sxs-lookup"><span data-stu-id="d6443-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="d6443-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6443-112">Examples</span></span>

<span data-ttu-id="d6443-113">O exemplo a seguir mostra como definir o **\_ \_ ProtectionScheme de criptografia MFSampleExtension** e os **atributos \_ \_ CryptByteBlock** de criptografia de MFSampleExtension e MFSampleExtension de criptografia de grupo de SkipByteBlock associados. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6443-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d6443-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6443-114">Requirements</span></span>



| <span data-ttu-id="d6443-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6443-115">Requirement</span></span> | <span data-ttu-id="d6443-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d6443-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6443-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6443-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6443-118">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="d6443-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d6443-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6443-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6443-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d6443-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d6443-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6443-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6443-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6443-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
