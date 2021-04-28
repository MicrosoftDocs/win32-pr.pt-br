---
description: Método UnlockWithPassphrase da classe Win32_EncryptableVolume – usa a frase secreta para obter a chave derivada.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116454"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithPassphrase da classe Win32 \_ EncryptableVolume

O método **UnlockWithPassphrase** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a frase secreta para obter a chave derivada. Depois que a chave derivada é calculada, a chave derivada é usada para desbloquear a chave mestra do volume criptografado.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Frase secreta* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica a frase secreta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                       | Descrição                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | O método foi bem-sucedido.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ impede a \_ senha**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | A configuração de política de grupo que requer conformidade com FIPS impediu que a frase secreta fosse gerada ou usada. <br/> |
| <dl> <dt>**FVE \_ E \_ \_ \_ \_ comprimento de senha inválido da política**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | A senha fornecida não atende aos requisitos mínimos ou máximos de comprimento.<br/>                              |
| <dl> <dt>**FVE \_ Senha da política de E \_ \_ \_ muito \_ simples**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | A senha não atende aos requisitos de complexidade definidos pelo administrador na diretiva de grupo.<br/>             |
| <dl> <dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | O volume não pode ser desbloqueado com as informações fornecidas. <br/>                                                  |
| <dl> <dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | O protetor de chave fornecido não existe no volume. Você deve inserir outro protetor de chave.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




