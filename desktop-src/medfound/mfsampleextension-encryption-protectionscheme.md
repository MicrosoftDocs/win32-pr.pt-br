---
description: Especifica o esquema de proteção para exemplos criptografados.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: MFSampleExtension_Encryption_ProtectionScheme atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9db7d00d67b0e9806167ea574d10c3dca5f199293c03f5e055d60430c2dd75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603176"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>Atributo MFSampleExtension \_ \_ Encryption ProtectionScheme

Especifica o esquema de proteção para exemplos criptografados.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da [**enumeração MFSampleEncryptionProtectionScheme.**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) Nos casos em que a fonte de mídia é baseada em **\_** MP4, o valor é definido com base no valor do campo de tipo de esquema dentro da caixa de tipo de esquema ('set') no header MP4 ('moov' ou 'moof').

Se **o \_** campo de tipo de esquema em um arquivo baseado em MP4 ou fluxo estiver definido como 'cenc' ou 'cbc1', o atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** deverá ser definido como PROTECTION **SCHEME \_ \_ AES \_ CTR** ou **PROTECTION SCHEME \_ \_ CBC,** respectivamente, e nenhum valor deverá ser definido para [ \_ \_ CryptByteBlock de Criptografia MFSampleExtension e](mfsampleextension-encryption-cryptbyteblock.md) [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).

Se o **campo de \_ tipo de** esquema em um arquivo baseado em MP4, ou stream, é definido como 'cens' ou 'cbcs', o atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** deve ser definido como **PROTECTION SCHEME \_ \_ AES \_ CTR** ou **PROTECTION SCHEME \_ \_ CBC**, respectivamente, e [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) e [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) devem ser definidos usando os valores na caixa 'tenc'.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir o **MFSampleExtension \_ Encryption \_ ProtectionScheme** e os atributos **de Criptografia MFSampleExtension \_ \_ CryptByteBlock** e **MFSampleExtension \_ \_ SkipByteBlock** associados.


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
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
