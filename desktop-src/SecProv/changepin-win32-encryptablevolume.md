---
description: Altera o PIN associado a um volume criptografado.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Método ChangePIN da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501536"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Método ChangePIN da classe Win32 \_ EncryptableVolume

O método **ChangePIN** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) altera o PIN associado a um volume criptografado. Se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, um PIN poderá conter letras, símbolos e espaços além dos números.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

O identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*NewPIN* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres de identificação pessoal especificada pelo usuário. Essa cadeia de caracteres deve consistir em uma sequência de 4 a 20 dígitos ou, se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, de 4 a 20 letras, símbolos, espaços ou números.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ inicializável \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Um CD/DVD inicializável foi encontrado neste computador. Remova o CD/DVD e reinicie o computador.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ caracteres de PIN inválidos**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | O parâmetro *NewPIN* contém caracteres que não são válidos. Quando a Política de Grupo "permitir PINs avançados para inicialização" está desabilitada, somente os números têm suporte.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>     | O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "senha numérica" ou "chave externa". Use o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar um protetor de chave do tipo apropriado.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | O volume está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Política E \_ \_ \_ comprimento de PIN inválido**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | O parâmetro *NewPIN* fornecido tem mais de 20 caracteres, menos de 4 caracteres ou menos que o comprimento mínimo especificado por política de grupo.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt> </dl>        | O protetor de chave fornecido não existe no volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt> </dl>        | Nenhum Trusted Platform Module compatível (TPM) encontrado neste computador.<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

O método **ChangePIN** cria um novo TPM e um protetor de PIN com base nas informações de protetor existentes e no PIN fornecido recentemente. O novo protetor terá o mesmo GUID. O método **ChangePIN** também pode ser chamado para alterar o PIN de qualquer protetor de chave que usa um PIN, por exemplo, TPM e PIN ou TPM com PIN e USB.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
