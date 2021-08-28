---
description: Indica o algoritmo de criptografia e o tamanho da chave usados no volume.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Método GetEncryptionMethod da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f9f4a2ad20af7c5ee3ba3afd8e2d9e56d0720b38d7afc2b01042e440cc85bf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892444"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Método GetEncryptionMethod da classe Win32 \_ EncryptableVolume

O método **GetEncryptionMethod** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica o algoritmo de criptografia e o tamanho da chave usados no volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncryptionMethod* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Um inteiro sem sinal que especifica o algoritmo de criptografia e o tamanho da chave usados no volume.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Nenhum**</dt> <dt>0</dt> </dl>                                | O volume não está criptografado.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ com \_ difusor**</dt> <dt>1</dt> </dl> | O volume foi totalmente ou parcialmente criptografado com o algoritmo de criptografia AES (AES) aprimorado com uma camada difusor, usando um tamanho de chave AES de 128 bits. esse método não está mais disponível em dispositivos que executam o Windows 8.1 ou superior.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ com \_ difusor**</dt> <dt>2</dt> </dl> | O volume foi totalmente ou parcialmente criptografado com o algoritmo de criptografia AES (AES) aprimorado com uma camada difusor, usando um tamanho de chave AES de 256 bits. esse método não está mais disponível em dispositivos que executam o Windows 8.1 ou superior.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | O volume foi totalmente ou parcialmente criptografado com o algoritmo criptografia AES (AES), usando um tamanho de chave AES de 128 bits.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | O volume foi totalmente ou parcialmente criptografado com o algoritmo criptografia AES (AES), usando um tamanho de chave AES de 256 bits.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**Hardware \_ do CRIPTOGRAFIA**</dt> <dt>5</dt> </dl>         | O volume foi totalmente ou parcialmente criptografado usando os recursos de hardware da unidade.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | O volume foi totalmente ou parcialmente criptografado com XTS usando o criptografia AES (AES) e um tamanho de chave AES de 128 bits. esse método só está disponível em dispositivos que executam o Windows 10, versão 1511 ou superior.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | O volume foi totalmente ou parcialmente criptografado com XTS usando o criptografia AES (AES) e um tamanho de chave AES de 256 bits. esse método só está disponível em dispositivos que executam o Windows 10, versão 1511 ou superior.<br/>                          |
| <dl> <dt>(UInt32) – 1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> O volume foi totalmente ou parcialmente criptografado com um algoritmo desconhecido e um tamanho de chave.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

O algoritmo de criptografia é configurado na unidade de criptografia automática. Uma cadeia de caracteres nula significa que o BitLocker está usando criptografia de software ou nenhum método de criptografia é relatado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Enterprise, \[ somente aplicativos de área de trabalho do vista Ultimate Windows\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
