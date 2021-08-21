---
description: Recupera a chave pública e a impressão digital do certificado para um protetor de chave pública.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Método GetKeyProtectorCertificate da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e947cb5fadefa6703ab4515ddd8d2a9daf1e7439e514e75c64d3b1e6e885aa0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892059"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorCertificate da classe Win32 \_ EncryptableVolume

O método **GetKeyProtectorCertificate** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera a [*chave pública*](../secgloss/p-gly.md) e a impressão digital do [*certificado*](../secgloss/c-gly.md) para um protetor de chave pública.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*PublicKey* \[ fora\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de bytes que especifica a chave pública.

</dd> <dt>

*CertThumbprint* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica a impressão digital do certificado.

</dd> <dt>

*Certtype* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Um inteiro sem sinal que especifica o tipo do protetor de chave. Esse inteiro é usado para diferenciar entre o DRA (agente de recuperação de dados) e os certificados de usuário.



| Valor                                                                        | Significado                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | O certificado é um DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | O certificado não é um DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                       | Descrição                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | O método foi bem-sucedido.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | O protetor de chave especificado não é um protetor de chave. Você deve inserir outro protetor de chave.<br/>            |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Esta unidade está bloqueada por Criptografia de Unidade de Disco BitLocker. Você deve desbloquear este volume no painel de controle. <br/> |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ \_Certificado de usuário de política E \_ \_ \_ necessário**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Política de Grupo requer o uso de um certificado de usuário, como um cartão inteligente.<br/>                           |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise, \[ somente os aplicativos de área de trabalho do Windows 7 Ultimate\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
