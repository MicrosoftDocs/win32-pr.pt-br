---
description: Faz backup dos dados de recuperação para Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Método BackupRecoveryInformationToActiveDirectory da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761998"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>Método BackupRecoveryInformationToActiveDirectory da classe Win32 \_ EncryptableVolume

O método **BackupRecoveryInformationToActiveDirectory** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) faz backup dos dados de recuperação para Active Directory. Esse método requer que um protetor de senha numérica esteja presente no volume. Política de Grupo também deve ser configurado para habilitar o backup de informações de recuperação para Active Directory.

## <a name="syntax"></a>Sintaxe


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado. Esse protetor de chave deve ser um protetor de senha numérica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                                    |
| <dl> <dt>**S \_ FALSO**</dt> <dt>1 (0x1)</dt> </dl>                                         | Política de Grupo não permite o armazenamento de informações de recuperação para Active Directory.<br/>                         |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                             |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | O protetor de chave especificado não é um protetor de chave numérica. Você deve inserir um protetor de senha numérica. <br/> |



 

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

 

 




