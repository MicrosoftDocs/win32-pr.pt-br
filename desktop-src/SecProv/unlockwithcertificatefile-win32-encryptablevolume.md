---
description: Usa o arquivo de certificado fornecido para obter a chave derivada e desbloquear o volume criptografado.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Método UnlockWithCertificateFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 576de5820e5b16b59a0b77659a4833a261ecd9ef8445306ce3d6f320c664f833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004224"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateFile da classe EncryptableVolume do Win32 \_

O **método UnlockWithCertificateFile** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) usa o arquivo de certificado fornecido para obter a chave derivada e desbloquear o volume criptografado. [](../secgloss/c-gly.md)

> [!Note]  
> Se o disco dá suporte à criptografia de hardware, essa função define o status da banda como "desbloqueado""

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica o local e o nome do arquivo .cer usado para recuperar a impressão digital do certificado. Um [*certificado*](../secgloss/e-gly.md) de criptografia deve ser exportado no formato .cer ( binário codificado por [*DER (Distinguished Encoding Rules)*](../secgloss/d-gly.md) [*X.509*](../secgloss/x-gly.md) ou X.509 codificado em Base 64). O certificado de criptografia pode ser gerado a partir da PKI da Microsoft, PKI de terceiros ou auto-assinado.

</dd> <dt>

*PIN* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres de identificação pessoal especificada pelo usuário. Essa cadeia de caracteres deve consistir em uma sequência de 4 a 20 dígitos. Essa cadeia de caracteres é usada para autenticar silenciosamente o KSP (provedor de [*armazenamento*](../secgloss/k-gly.md) de chaves) quando usado com um [*cartão inteligente*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**ERRO \_ ARQUIVO \_ NÃO \_ ENCONTRADO**</dt> <dt>0000000002 (0x2)</dt> </dl>                 | O sistema não pode arquivar o arquivo especificado.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ FALHA \_ NA AUTENTICAÇÃO**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>   | O volume não pode ser desbloqueado com as informações fornecidas. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ E \_ PROTECTOR NÃO ENCONTRADO \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | O protetor de chave fornecido não existe no volume. Você deve inserir outro protetor de chave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | A [*chave privada*](../secgloss/p-gly.md), associada ao certificado especificado, não pôde ser autorizada. A autorização de chave privada não foi fornecida ou a autorização fornecida foi inválida.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise, Windows 7 aplicativos de área de \[ trabalho ultimate\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                 |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
