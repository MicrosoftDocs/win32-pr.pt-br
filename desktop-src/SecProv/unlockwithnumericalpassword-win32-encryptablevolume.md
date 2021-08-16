---
description: Usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Método UnlockWithNumericalPassword da classe Win32_EncryptableVolume dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d52cd0dd2c80bf00a55bef0fde40008f7133f28cb3be0a9aa5366076c6502b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891290"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithNumericalPassword da classe EncryptableVolume do Win32 \_

O **método UnlockWithNumericalPassword** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.

A chave de criptografia do volume deve ter sido protegida com um ou mais protetores de chave do tipo "Senha Numérica" (usando o [**método ProtectKeyWithNumericalPassword)**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para poder desbloquear o volume com esse método.

> [!Note]  
> Se o disco dá suporte à criptografia de hardware, essa função define o status da banda como "desbloqueado""

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumericalPassword* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica a senha numérica.

A senha numérica deve conter 48 dígitos. Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo indicando um valor de verificação para o grupo. Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 65536. Supondo que um grupo de seis dígitos seja rotulado como x1, x2, x3, x4, x5 e x6, o dígito de checksum x6 é calculado como –x1+x2-x3+x4-x5 mod 11.

Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen. Portanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" ou "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" também pode conter senhas numéricas válidas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se o volume já estiver desbloqueado e nenhum outro erro ocorrer, esse método retornará 0.



| Valor/código de retorno                                                                                                                                                                             | Descrição                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | O método foi bem-sucedido.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ PROTECTOR NÃO ENCONTRADO \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>     | O volume não tem um protetor de chave do tipo "Senha Numérica".<br/> O *parâmetro NumericalPassword* tem um formato válido, mas você não pode usar uma senha numérica para desbloquear o volume.<br/>           |
| <dl> <dt>**FVE \_ E \_ FALHA \_ NA AUTENTICAÇÃO**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>    | O *parâmetro NumericalPassword* não pode desbloquear o volume.<br/> Existe um ou mais protetores de chave do tipo "Senha Numérica", mas o parâmetro *NumericalPassword* especificado não pode desbloquear o volume.<br/> |
| <dl> <dt>**FVE \_ E \_ FORMATO \_ DE \_ SENHA**</dt> <dt>INVÁLIDO 2150694965 (0x80310035)</dt> </dl> | O *parâmetro NumericalPassword* não tem um formato válido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Windows SDK. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows aplicativos da área de trabalho do Vista Ultimate \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
