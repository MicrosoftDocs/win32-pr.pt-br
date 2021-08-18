---
description: Indica se a senha numérica atende aos requisitos de formato especial para esse valor de autenticação.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Método IsNumericalPasswordValid da classe Win32_EncryptableVolume dados
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
ms.openlocfilehash: 0aed00554d7a8e284f83659dc92266b1ce5e098f1b102e6444bfc07fd2909066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739636"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Método IsNumericalPasswordValid da classe EncryptableVolume do Win32 \_

O **método IsNumericalPasswordValid** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) indica se a senha numérica atende aos requisitos de formato especial para esse valor de autenticação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumericalPassword* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica a senha numérica.

A senha numérica deve conter 48 dígitos. Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo indicando um valor de verificação para o grupo. Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 720896. Supondo que um grupo de seis dígitos seja rotulado como x1, x2, x3, x4, x5 e x6, o dígito de checksum x6 é calculado como –x1+x2-x3+x4-x5 mod 11.

Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen. Portanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" ou "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" também pode conter senhas numéricas válidas.

</dd> <dt>

*IsNumericalPasswordValid* \[ out\]
</dt> <dd>

Tipo: **booliana**

Um valor booliana que será verdadeiro se a senha numérica atender aos requisitos de formato especial para esse valor de autenticação, caso contrário, o valor será false.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
