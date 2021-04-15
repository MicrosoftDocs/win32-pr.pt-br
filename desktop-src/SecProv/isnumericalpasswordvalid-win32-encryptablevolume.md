---
description: Indica se a senha numérica atende aos requisitos de formato especiais para esse valor de autenticação.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Método IsNumericalPasswordValid da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761386"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Método IsNumericalPasswordValid da classe Win32 \_ EncryptableVolume

O método **IsNumericalPasswordValid** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se a senha numérica atende aos requisitos de formato especiais para esse valor de autenticação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumericalPassword* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica a senha numérica.

A senha numérica deve conter 48 dígitos. Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo, indicando um valor de soma de verificação para o grupo. Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 720896. Supondo que um grupo de seis dígitos seja rotulado como X1, X2, X3, x4, X5 e X6, o dígito de soma de verificação X6 é calculado como – X1 + X2 – X3 + X4 – X5 mod 11.

Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen. Portanto, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" ou "XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX, XXXXXX XXXXXX", também pode conter senhas numéricas válidas.

</dd> <dt>

*IsNumericalPasswordValid* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Um valor booliano que será true se a senha numérica atender aos requisitos de formato especiais para esse valor de autenticação; caso contrário, o valor será false.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

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

 

 
