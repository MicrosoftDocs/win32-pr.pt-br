---
description: Usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Método UnlockWithNumericalPassword da classe Win32_EncryptableVolume
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
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826967"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithNumericalPassword da classe Win32 \_ EncryptableVolume

O método **UnlockWithNumericalPassword** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.

A chave de criptografia do volume deve ter sido protegida com um ou mais protetores de chave do tipo "senha numérica" (usando o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) para poder desbloquear o volume com esse método.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumericalPassword* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica a senha numérica.

A senha numérica deve conter 48 dígitos. Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo, indicando um valor de soma de verificação para o grupo. Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 65536. Supondo que um grupo de seis dígitos seja rotulado como X1, X2, X3, x4, X5 e X6, o dígito de soma de verificação X6 é calculado como – X1 + X2 – X3 + X4 – X5 mod 11.

Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen. Portanto, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" ou "XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX, XXXXXX XXXXXX", também pode conter senhas numéricas válidas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se o volume já estiver desbloqueado e nenhum outro erro ocorrer, esse método retornará 0.



| Código/valor de retorno                                                                                                                                                                             | Descrição                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | O método foi bem-sucedido.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | O volume não tem um protetor de chave do tipo "senha numérica".<br/> O parâmetro *NumericalPassword* tem um formato válido, mas você não pode usar uma senha numérica para desbloquear o volume.<br/>           |
| <dl> <dt>**FVE \_ E \_ \_ autenticação com falha**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | O parâmetro *NumericalPassword* não pode desbloquear o volume.<br/> Existe um ou mais protetores de chave do tipo "senha numérica", mas o parâmetro *NumericalPassword* especificado não pode desbloquear o volume.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ \_ formato de senha inválido**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | O parâmetro *NumericalPassword* não tem um formato válido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]<br/>                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
