---
description: Desabilita ou suspende todos os protetores de chave associados a este volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Método DisableKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761388"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DisableKeyProtectors da classe Win32 \_ EncryptableVolume

O método **DisableKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) desabilita ou suspende todos os protetores de chave associados a esse volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DisableCount* \[ em, opcional\]
</dt> <dd>

Tipo: **UInt32**

Inteiro que especifica o número de reinicializações para as quais os protetores de chave serão desabilitados. Esse parâmetro só está disponível em volumes do sistema operacional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                  | Descrição                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>      |



 

## <a name="security-considerations"></a>Considerações de segurança

Esse método expõe a chave de criptografia do volume em Clear no disco rígido, desativando qualquer proteção de volume. É recomendável que você tenha qualquer senha ou chave de criptografia em texto sem formatação.

## <a name="remarks"></a>Comentários

Novos protetores de chave podem ser adicionados mesmo quando protetores de chave estão desabilitados ou suspensos. Esses protetores de chave permanecerão desabilitados, a menos que [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) seja chamado.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
