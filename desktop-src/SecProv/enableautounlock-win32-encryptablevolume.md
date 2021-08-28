---
description: Permite que um volume de dados seja desbloqueado automaticamente quando o volume é montado.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Método EnableAutoUnlock da Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 712a5460769009f9e10e2b9730ad78632bc5ad10c2af2d1eaf63bcb2c91d7c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892454"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Método EnableAutoUnlock da classe EncryptableVolume do Win32 \_

O **método EnableAutoUnlock** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) permite que um volume de dados seja desbloqueado automaticamente quando o volume é montado.

O desbloqueio automático salva uma chave externa no sistema operacional que pode desbloquear automaticamente o volume no volume do sistema operacional em execução no momento.

Para usar esse método, o volume do sistema operacional já deve ser protegido pelo Criptografia de Unidade de Disco BitLocker ou deve ter criptografia em andamento. Além disso, já deve existir uma chave externa para o volume de dados. Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar a chave externa que pode desbloquear automaticamente o volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que identifica o protetor de chave do tipo "Chave Externa" usado para desbloquear automaticamente o volume.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                           | Descrição                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | O método foi bem-sucedido.<br/>                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>          | O volume está bloqueado.<br/>                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl>          | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | O *parâmetro VolumeKeyProtectorID* não se refere a um protetor de chave válido do tipo "Chave Externa".<br/>                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | O método não pode ser executado para o volume do sistema operacional em execução no momento.<br/>                                                                                       |
| <dl> <dt>**FVE \_ SISTEMA \_ \_ OPERACIONAL NÃO \_ PROTEGIDO**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | O método não poderá ser executado se o volume do sistema operacional em execução no momento não estiver protegido pelo Criptografia de Unidade de Disco BitLocker ou não tiver criptografia em andamento.<br/> |
| <dl> <dt> **FVE \_ E VOLUME BOUND \_ \_ \_ JÁ**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | O desbloqueio automático no volume foi habilitado anteriormente.<br/>                                                                                                    |



 

## <a name="remarks"></a>Comentários

Dado um protetor de chave de volume válido do tipo "Chave Externa", a chave externa de 256 bits relacionada é extraída do protetor e armazenada no registro do sistema operacional em execução no momento, juntamente com a ID do protetor de chave de volume.

Se a chave externa associada à ID do protetor de chave de volume for excluída, a funcionalidade para desbloquear automaticamente o volume será desabilitada ou suspensa.

> [!Note]  
> Atualmente, não há suporte para mídia removível.

 

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

 

 
