---
description: Inicia a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Método descriptografar da classe Win32_EncryptableVolume (Infocard.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e9018cfab8bea6c149c4771a54dbe55a62afafd447f4db2e162aa76d183c28ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004624"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Método Descriptografar da classe EncryptableVolume do Win32 \_

O **método Decrypt** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) inicia a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.

Quando a descriptografia é pausada ou em andamento, esse método se comporta da mesma forma que [**ResumeConversion.**](resumeconversion-win32-encryptablevolume.md) Quando a criptografia é pausada ou em andamento, esse método reverte a criptografia e inicia a descriptografia. Após a conclusão da descriptografia, todos os protetores de chave nesse volume são removidos do sistema e o volume é convertido em um sistema de arquivos NTFS padrão.

> [!Note]  
> Se o disco for criptografado por hardware, o método **Descriptografar** define o status da banda como "sempre desbloqueado", remove todos os metadados associados e zera a ID de segurança da unidade.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Esse método retorna imediatamente. Se o volume já estiver totalmente descriptografado e nenhum outro erro existir, esse método retornará 0.



| Valor/código de retorno                                                                                                                                                                       | Descrição                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | O método foi bem-sucedido.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | O volume está bloqueado.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ AUTOUNLOCK \_ HABILITADO 2150694953**</dt> <dt>(0x80310029)</dt> </dl> | Esse volume não pode ser descriptografado porque as chaves usadas para desbloquear automaticamente os volumes de dados estão disponíveis. <br/> Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para remover essas chaves.<br/> |



 

## <a name="security-considerations"></a>Considerações de segurança

Chamar o **método Decrypt** deixa os dados desprotegidos.

Se o status de proteção do volume for 1 (PROTECTION ON) antes que esse método seja usado, a conclusão bem-sucedida desse método altera o status de proteção para 0 (PROTECTION OFF), já que, por definição, um volume parcialmente criptografado não é protegido.

## <a name="remarks"></a>Comentários

Se o volume ainda não estiver totalmente descriptografado, a execução de **Descriptografar** faz com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a descriptografia está em andamento e mostra o percentual do volume que permanece criptografado.

Se o status de proteção do volume estiver "ligado" antes que esse método seja executado, a execução desse método altera o status de proteção para "off", já que, por definição, um volume parcialmente criptografado não está protegido.

Se esse método for executado no volume do sistema operacional em execução no momento e esse volume do sistema operacional estiver sendo usado para desbloquear automaticamente os volumes de dados (consulte o método [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), primeiro você deverá chamar o método [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows aplicativos da área de trabalho do Vista Ultimate \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>Infocard.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
