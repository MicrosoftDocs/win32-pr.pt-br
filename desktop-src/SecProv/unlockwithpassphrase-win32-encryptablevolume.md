---
description: Método UnlockWithPassphrase da classe Win32_EncryptableVolume - usa a frase-senha para obter a chave derivada.
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
ms.openlocfilehash: 7b8a1ef65fd1ca3e279631a1add00ad7c07e2ff870bc24c883fd1877a3800d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004164"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithPassphrase da classe EncryptableVolume do Win32 \_

O **método UnlockWithPassphrase** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) usa a frase-chave para obter a chave derivada. Depois que a chave derivada é calculada, a chave derivada é usada para desbloquear a chave mestra do volume criptografado.

> [!Note]  
> Se o disco dá suporte à criptografia de hardware, essa função define o status da banda como "desbloqueado""

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Frase-senha* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica a frase-senha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                                       | Descrição                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | O método foi bem-sucedido.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl>                      | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ IMPEDE A 2150695020 \_ SENHA**</dt> <dt>(0x8031006C)</dt> </dl>          | A configuração de política de grupo que requer conformidade com FIPS impediu que a frase-senha fosse gerada ou usada. <br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | A frase-senha fornecida não atendem aos requisitos mínimos ou máximos de comprimento.<br/>                              |
| <dl> <dt>**FVE \_ SENHA DE POLÍTICA DE E \_ \_ MUITO \_ \_ SIMPLES**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | A frase-senha não atendem aos requisitos de complexidade definidos pelo administrador na política de grupo.<br/>             |
| <dl> <dt>**FVE \_ E \_ FALHA \_ NA AUTENTICAÇÃO**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>              | O volume não pode ser desbloqueado com as informações fornecidas. <br/>                                                  |
| <dl> <dt>**FVE \_ E \_ PROTECTOR NÃO ENCONTRADO \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>               | O protetor de chave fornecido não existe no volume. Você deve inserir outro protetor de chave.<br/>                 |



 

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

 

 




