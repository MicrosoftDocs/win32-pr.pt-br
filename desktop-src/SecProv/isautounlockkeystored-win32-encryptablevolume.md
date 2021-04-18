---
description: Indica se as chaves externas ou as informações relacionadas que podem ser usadas para desbloquear automaticamente os volumes de dados existem no volume do sistema operacional em execução no momento.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Método IsAutoUnlockKeyStored da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760372"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockKeyStored da classe Win32 \_ EncryptableVolume

O método **IsAutoUnlockKeyStored** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se as chaves externas ou as informações relacionadas que podem ser usadas para desbloquear automaticamente os volumes de dados existem no volume do sistema operacional em execução no momento.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsAutoUnlockKeyStored* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Será **true** se qualquer informação que possa ser usada para desbloquear automaticamente os volumes de dados estiver armazenada no registro do volume do sistema operacional em execução no momento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                   | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ não \_ o \_ VOLUME do so**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | O método só pode ser executado para o volume do sistema operacional em execução no momento.<br/>     |



 

## <a name="remarks"></a>Comentários

Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para remover todas as informações de desbloqueio do volume do sistema operacional em execução no momento.

As informações usadas para desbloquear um volume são armazenadas quando o [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) é executado para um volume de dados enquanto o volume do sistema operacional atualmente em execução está em execução.

**IsAutoUnlockKeyStored** difere de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) , mesmo se o desbloqueio automático estiver desabilitado para todos os volumes de dados atualmente conectados ao computador, ainda poderá haver desbloqueio de informações associadas a volumes de dados desconectados ou volumes de dados que não existem mais.

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

 

 
