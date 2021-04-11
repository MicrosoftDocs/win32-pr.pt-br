---
description: Indica se os protetores estão disponíveis para o volume.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Método IsKeyProtectorAvailable da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164389"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a>Método IsKeyProtectorAvailable da classe Win32 \_ EncryptableVolume

O método **IsKeyProtectorAvailable** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se os protetores estão disponíveis para o volume.

Se um tipo de protetor for fornecido, o método indicará se os protetores do tipo especificado estão disponíveis para o volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Keyprotetortype* \[ em, opcional\]
</dt> <dd>

Tipo: **UInt32**

Um inteiro sem sinal que indica o tipo de protetor de chave de volume consultado.

Se esse parâmetro não for especificado, todos os protetores de chave disponíveis do volume serão consultados.



| Valor                                                                         | Significado                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Todos os tipos.<br/> Todos os protetores de chave são consultados.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                        |
| <dl> <dt>2</dt> </dl>  | Chave externa.<br/>                                         |
| <dl> <dt>3</dt> </dl>  | Senha numérica.<br/>                                   |
| <dl> <dt>4</dt> </dl>  | TPM e PIN.<br/>                                          |
| <dl> <dt>5</dt> </dl>  | TPM e chave de inicialização.<br/>                                  |
| <dl> <dt>6</dt> </dl>  | TPM e PIN e chave de inicialização.<br/>                          |
| <dl> <dt>7</dt> </dl>  | Chave pública.<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Senha.<br/>                                           |
| <dl> <dt>9</dt> </dl>  | Certificado TPM<br/>                                       |
| <dl> <dt>10</dt> </dl> | Identificador de segurança (SID)<br/>                             |



 

</dd> <dt>

*IsKeyProtectorAvailable* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Um valor booliano que indica se um protetor de chave de volume do tipo especificado existe no volume.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                         | Descrição                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                         | O método foi bem-sucedido.<br/>                                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl> | O parâmetro *Keyprotetortype* é especificado, mas não se refere a um tipo de protetor de chave válido.<br/> |



 

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

 

 
