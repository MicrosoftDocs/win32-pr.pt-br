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
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>Atributo MFSampleExtension de \_ criptografia \_ ProtectionScheme

Especifica o esquema de proteção para exemplos criptografados.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da enumeração [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) . Nos casos em que a origem da mídia é baseada em MP4, o valor é definido com base no valor do campo **\_ tipo de esquema** na caixa tipo de esquema (' schm ') no cabeçalho MP4 (' Moov ' ou ' Moof ').

Se o **campo \_ tipo de esquema** em um arquivo baseado em MP4, ou fluxo, for definido como ' Cenc ' ou ' cbc1 ', o **atributo \_ \_ ProtectionScheme de criptografia MFSampleExtension** deverá ser definido como **esquema de proteção \_ \_ AES \_ CTR** ou o **esquema de proteção \_ \_ CBC**, respectivamente, e nenhum valor deve ser definido para MFSampleExtension [ \_ Encryption \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock e [MFSampleExtension \_ Encryption \_](mfsampleextension-encryption-skipbyteblock.md)SkipByteBlock.

Se o **campo \_ tipo de esquema** em um arquivo baseado em MP4, ou fluxo, for definido como ' Cens ' ou ' CBCs ', o **atributo \_ \_ ProtectionScheme de criptografia MFSampleExtension** deverá ser definido como **esquema de proteção \_ \_ AES \_ CTR** ou o **esquema de proteção \_ \_ CBC**, respectivamente, e MFSampleExtension [ \_ criptografia \_](mfsampleextension-encryption-cryptbyteblock.md) CryptByteBlock e MFSampleExtension [ \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) devem ser definidos usando os valores na caixa ' tenc '.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir o **\_ \_ ProtectionScheme de criptografia MFSampleExtension** e os **atributos \_ \_ CryptByteBlock** de criptografia de MFSampleExtension e MFSampleExtension de criptografia de grupo de SkipByteBlock associados. **\_ \_**


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
