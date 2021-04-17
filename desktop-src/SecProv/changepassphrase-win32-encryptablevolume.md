---
description: Usa a nova senha para obter uma nova chave derivada.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Método ChangePassphrase da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780155"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a>Método ChangePassphrase da classe Win32 \_ EncryptableVolume

O método **ChangePassphrase** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a nova senha para obter uma nova chave derivada. Depois que a chave derivada é calculada, a nova chave derivada é usada para proteger a chave mestra do volume criptografado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo que é usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*NewPassphrase* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres atualizada que especifica a frase secreta.

</dd> <dt>

*NewProtectorID* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo atualizado usado para gerenciar um protetor de chave de volume criptografado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                       | Descrição                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | O método foi bem-sucedido.<br/>                                                                                  |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | O volume já está bloqueado por Criptografia de Unidade de Disco BitLocker. Você deve desbloquear a unidade no painel de controle.<br/>   |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                           |
| <dl> <dt>**FVE \_ \_ \_ Atualização do E Overlapped**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                  | O bloco de controle do volume criptografado foi atualizado por outro thread.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>            | O protetor de chave especificado não é do tipo correto. <br/>                                                    |
| <dl> <dt>**FVE \_ E \_ \_ \_ \_ comprimento de senha inválido da política**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | A senha atualizada fornecida não atende aos requisitos mínimos ou máximos de comprimento. <br/>                  |
| <dl> <dt>**FVE \_ Senha da política de E \_ \_ \_ muito \_ simples**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | A senha atualizada não atende aos requisitos de complexidade definidos pelo administrador na diretiva de grupo. <br/> |



 

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

 

 




