---
description: Método ProtectKeyWithPassphrase da classe Win32_EncryptableVolume – usa a frase secreta para obter a chave derivada.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Método ProtectKeyWithPassphrase da classe Win32_EncryptableVolume
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
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098344"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithPassphrase da classe Win32 \_ EncryptableVolume

O método **ProtectKeyWithPassphrase** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a frase secreta para obter a chave derivada. Depois que a chave derivada é calculada, a chave derivada é usada para proteger a chave mestra do volume criptografado.

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

*FriendlyName* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave. Se esse parâmetro não for especificado, um valor em branco será usado.

</dd> <dt>

*Frase secreta* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica a frase secreta.

</dd> <dt>

*VolumeKeyProtectorID* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado.

Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                        | Descrição                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | O método foi bem-sucedido.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ não \_ é \_ permitido \_ no \_ modo de segurança**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Criptografia de Unidade de Disco BitLocker só pode ser usado para fins de recuperação quando usado no modo de segurança.<br/>                     |
| <dl> <dt>**FVE \_ \_Senha da política E \_ \_ não \_ permitida**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | A política de grupo não permite a criação de uma frase secreta.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ impede a \_ senha**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | A configuração de política de grupo que requer conformidade com FIPS impediu que a frase secreta fosse gerada ou usada.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ \_ \_ comprimento de senha inválido da política**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | A senha fornecida não atende aos requisitos mínimos ou máximos de comprimento.<br/>                             |
| <dl> <dt>**FVE \_ Senha da política de E \_ \_ \_ muito \_ simples**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | A senha não atende aos requisitos de complexidade definidos pelo administrador na diretiva de grupo.<br/>            |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | O volume já está bloqueado por Criptografia de Unidade de Disco BitLocker. Você deve desbloquear a unidade no painel de controle.<br/>     |
| <dl> <dt>**FVE \_ \_ \_ Atualização do E Overlapped**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | O bloco de controle do volume criptografado foi atualizado por outro thread.<br/>                                     |
| <dl> <dt>**FVE \_ \_ \_ \_ Não \_ há suporte para o protetor de chave E**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | O protetor de chave não tem suporte na versão do Criptografia de Unidade de Disco BitLocker atualmente no volume.<br/>      |
| <dl> <dt>**FVE \_ \_Senha de volume do so E \_ \_ \_ não \_ permitida**</dt> <dt>2150695021 (0x8031006D)</dt> </dl> | A senha não pode ser adicionada ao volume do sistema operacional. <br/>                                               |
| <dl> <dt>**FVE \_ O \_ protetor E \_ existe**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | O protetor de chave fornecido já existe neste volume.<br/>                                                     |



 

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

 

 




