---
description: Usa a impressão digital do certificado fornecida para obter a chave derivada e desbloquear o volume criptografado.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Método UnlockWithCertificateThumbprint da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0ccf4a68f999bee1d32d8025759eb9625371b18fc5028b54e68e62df544bbd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891361"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateThumbprint da classe EncryptableVolume do Win32 \_

O **método UnlockWithCertificateThumbprint** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) usa a impressão digital do certificado fornecida para obter a chave derivada e desbloquear o volume criptografado. [](../secgloss/c-gly.md)

> [!Note]  
> Se o disco dá suporte à criptografia de hardware, essa função define o status da banda como "desbloqueado""

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CertThumbprint* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um valor de impressão digital de 0 é aceito e resulta em uma pesquisa no armazenamento local para o certificado apropriado. Se um único certificado BitLocker for encontrado, a pesquisa será bem-sucedida. Se nenhum ou mais de um certificado for encontrado, o método falhará.

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
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ FALHA \_ NA AUTENTICAÇÃO**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>   | O volume não pode ser desbloqueado usando as informações fornecidas. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ PROTECTOR NÃO ENCONTRADO \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | O protetor de chave fornecido não existe no volume. Você deve inserir outro protetor de chave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Não [*foi possível*](../secgloss/p-gly.md) autorizar a chave privada associada ao certificado especificado. A autorização de chave privada não foi fornecida ou a autorização fornecida não era válida.<br/> |



 

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

 

 
