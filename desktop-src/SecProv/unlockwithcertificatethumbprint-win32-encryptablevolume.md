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
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646981"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateThumbprint da classe Win32 \_ EncryptableVolume

O método **UnlockWithCertificateThumbprint** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a impressão digital do [*certificado*](../secgloss/c-gly.md) fornecida para obter a chave derivada e desbloquear o volume criptografado.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CertThumbprint* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um valor de impressão digital 0 é aceito e resulta em uma pesquisa do repositório local para o certificado apropriado. Se um único certificado do BitLocker for encontrado, a pesquisa será bem-sucedida. Se nenhum ou mais de um certificado for encontrado, o método falhará.

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
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | O volume não pode ser desbloqueado usando as informações fornecidas. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | O protetor de chave fornecido não existe no volume. Você deve inserir outro protetor de chave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Falha de \_ autenticação \_ do E PRIVATEKEY**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Não foi possível autorizar a [*chave privada*](../secgloss/p-gly.md) associada ao certificado especificado. A autorização de chave privada não foi fornecida ou a autorização fornecida não era válida.<br/> |



 

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

 

 
