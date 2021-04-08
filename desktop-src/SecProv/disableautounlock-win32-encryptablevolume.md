---
description: Remove a chave externa salva no volume do sistema operacional em execução no momento.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Método DisableAutoUnlock da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828547"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Método DisableAutoUnlock da classe Win32 \_ EncryptableVolume

O método **DisableAutoUnlock** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) remove a chave externa salva no volume do sistema operacional em execução no momento para que um volume de dados não seja desbloqueado automaticamente quando montado, como quando os dispositivos de memória removível estão conectados ao computador.

Se o desbloqueio automático estiver desabilitado ou suspenso, os métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) deverão ser usados para desbloquear o volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                       | Descrição                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | O método foi bem-sucedido.<br/>                                                       |
| <dl> <dt> **FVE \_ E \_ volume \_ não \_ associado**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | O desbloqueio automático no volume está desabilitado.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ não \_ \_ VOLUME de dados**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | O método não pode ser executado para o volume do sistema operacional em execução no momento.<br/>      |



 

## <a name="remarks"></a>Comentários

Se nenhum erro for retornado, esse método removerá do registro quaisquer IDs de protetor de volume e chaves externas usadas para desbloquear automaticamente o volume.

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

 

 
