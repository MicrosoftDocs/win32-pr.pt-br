---
description: Método ProtectKeyWithPassphrase da classe Win32_EncryptableVolume - usa a frase-senha para obter a chave derivada.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Método ProtectKeyWithPassphrase da Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c0d87eb21ea505b13ce3aacfe8be6ff1fa9d266ba2a781d6b8e6fc4d77dac10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004354"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithPassphrase da classe EncryptableVolume do Win32 \_

O **método ProtectKeyWithPassphrase** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) usa a frase-senha para obter a chave derivada. Depois que a chave derivada é calculada, a chave derivada é usada para proteger a chave mestra do volume criptografado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyName* \[ in, opcional\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave. Se esse parâmetro não for especificado, um valor em branco será usado.

</dd> <dt>

*Frase-senha* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica a frase-senha.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado.

Se a unidade for compatível com criptografia de hardware e o BitLocker não tiver assumido a propriedade da banda, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado em metadados por banda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                                        | Descrição                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | O método foi bem-sucedido.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ NÃO PERMITIDO NO MODO DE \_ \_ \_ \_ SEGURANÇA**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Criptografia de Unidade de Disco BitLocker pode ser usado somente para fins de recuperação quando usado no Cofre.<br/>                     |
| <dl> <dt>**FVE \_ FRASE-SENHA DE \_ \_ POLÍTICA NÃO PERMITIDA \_ \_ 2150695018**</dt> <dt>(0x8031006A)</dt> </dl>     | A política de grupo não permite a criação de uma frase-senha.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ IMPEDE A 2150695020 \_ SENHA**</dt> <dt>(0x8031006C)</dt> </dl>           | A configuração de política de grupo que requer conformidade com FIPS impediu que a frase-senha fosse gerada ou usada.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | A frase-senha fornecida não atendem aos requisitos mínimos ou máximos de comprimento.<br/>                             |
| <dl> <dt>**FVE \_ SENHA DE POLÍTICA DE E \_ \_ MUITO \_ \_ SIMPLES**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | A frase-senha não atendem aos requisitos de complexidade definidos pelo administrador na política de grupo.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | O volume já está bloqueado por Criptografia de Unidade de Disco BitLocker. Você deve desbloquear a unidade de Painel de Controle.<br/>     |
| <dl> <dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | O bloco de controle para o volume criptografado foi atualizado por outro thread.<br/>                                     |
| <dl> <dt>**FVE \_ PROTETOR DE CHAVE E \_ \_ SEM SUPORTE \_ \_ 2150695017**</dt> <dt>(0x80310069)</dt> </dl>       | O protetor de chave não é suportado pela versão do Criptografia de Unidade de Disco BitLocker no volume no momento.<br/>      |
| <dl> <dt>**FVE \_ E \_ A \_ \_ FRASE-SENHA DO VOLUME \_ \_**</dt> DO SISTEMA OPERACIONAL NÃO <dt>2150695021 (0x8031006D)</dt> </dl> | A frase-senha não pode ser adicionada ao volume do sistema operacional. <br/>                                               |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS 2150694960**</dt> <dt>(0x80310030)</dt> </dl>                    | O protetor de chave fornecido já existe nesse volume.<br/>                                                     |



 

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

 

 




