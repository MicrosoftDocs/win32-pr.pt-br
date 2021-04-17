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
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754119"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateFile da classe Win32 \_ EncryptableVolume

O método **UnlockWithCertificateFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa o arquivo de [*certificado*](../secgloss/c-gly.md) fornecido para obter a chave derivada e desbloquear o volume criptografado.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica o local e o nome do arquivo. cer usado para recuperar a impressão digital do certificado. Um certificado de [*criptografia*](../secgloss/e-gly.md) deve ser exportado no formato. cer ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) – binário codificado [*x. 509*](../secgloss/x-gly.md) ou x. 509 codificado em base-64). O certificado de criptografia pode ser gerado por meio da PKI da Microsoft, PKI de terceiros ou autoassinado.

</dd> <dt>

*Fixar* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres de identificação pessoal especificada pelo usuário. Essa cadeia de caracteres deve consistir em uma sequência de 4 a 20 dígitos. Essa cadeia de caracteres é usada para autenticar silenciosamente o KSP ( [*provedor de armazenamento de chaves*](../secgloss/k-gly.md) ) quando usado com um [*cartão inteligente*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**Erro \_ do ARQUIVO \_ não \_ encontrado**</dt> <dt>0000000002 (0x2)</dt> </dl>                 | O sistema não pode arquivar o arquivo especificado.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | O volume não pode ser desbloqueado com as informações fornecidas. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | O protetor de chave fornecido não existe no volume. Você deve inserir outro protetor de chave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Falha de \_ autenticação \_ do E PRIVATEKEY**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | A [*chave privada*](../secgloss/p-gly.md), associada ao certificado especificado, não pôde ser autorizada. A autorização de chave privada não foi fornecida ou a autorização fornecida era inválida.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
