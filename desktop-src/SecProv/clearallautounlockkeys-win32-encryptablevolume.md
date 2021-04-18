---
description: Remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usadas para desbloquear automaticamente os volumes de dados.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Método ClearAllAutoUnlockKeys da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761852"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Método ClearAllAutoUnlockKeys da classe Win32 \_ EncryptableVolume

O método **ClearAllAutoUnlockKeys** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usadas para desbloquear automaticamente os volumes de dados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                   | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ não \_ o \_ VOLUME do so**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | O método só pode ser executado para o volume do sistema operacional em execução no momento.<br/>     |



 

## <a name="remarks"></a>Comentários

O **ClearAllAutoUnlockKeys** Obtém a mesma funcionalidade que a execução de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para cada volume de dados que já foi associado ao sistema operacional em execução no momento, até mesmo os volumes de dados que não estão conectados ao computador no momento. Ele também remove quaisquer informações desbloqueadas obsoletas associadas a volumes de dados que não existem mais.

Antes de chamar a [**descriptografia**](decrypt-win32-encryptablevolume.md) no volume do sistema operacional em execução no momento, use **ClearAllAutoUnlockKeys** para garantir que as informações colocadas no registro do sistema operacional desbloqueiem automaticamente os volumes de dados não estejam acessíveis no disco limpo.

Depois que o **ClearAllAutoUnlockKeys** é executado com êxito, os métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) podem ser usados para desbloquear todos os volumes de dados neste computador. Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para reabilitar o desbloqueio automático de um volume de dados.

Se nenhum outro erro for retornado, o **ClearAllAutoUnlockKeys** removerá do registro quaisquer IDs de protetor de volume e chaves externas usadas para desbloquear automaticamente qualquer volume de dados que já tenha sido associado ao volume do sistema operacional em execução no momento.

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

 

 
