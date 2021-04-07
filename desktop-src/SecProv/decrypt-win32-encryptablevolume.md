---
description: Começa a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Método Decrypt da classe Win32_EncryptableVolume (InfoCard. h)
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
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828548"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Método Decrypt da classe Win32 \_ EncryptableVolume

O método **Decrypt** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) começa a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.

Quando a descriptografia é pausada ou em andamento, esse método se comporta da mesma forma que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Quando a criptografia é pausada ou em andamento, esse método reverte a criptografia e começa a descriptografia. Após a conclusão da descriptografia, todos os protetores de chave nesse volume serão removidos do sistema e o volume será convertido em um sistema de arquivos NTFS padrão.

> [!Note]  
> Se o disco estiver criptografado para hardware, o método **Decrypt** definirá o status da banda como "Always undeleted", removerá todos os metadados associados e zerará a ID de segurança da unidade.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Esse método retorna imediatamente. Se o volume já tiver sido totalmente descriptografado e nenhum outro erro existir, esse método retornará 0.



| Código/valor de retorno                                                                                                                                                                       | Descrição                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | O método foi bem-sucedido.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | O volume está bloqueado.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ E & \_ desbloqueio automático \_ habilitado**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | Este volume não pode ser descriptografado porque as chaves usadas para desbloquear automaticamente os volumes de dados estão disponíveis. <br/> Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para remover essas chaves.<br/> |



 

## <a name="security-considerations"></a>Considerações de segurança

Chamar o método **Decrypt** deixa os dados desprotegidos.

Se o status de proteção do volume for 1 (proteção ATIVAda) antes desse método ser usado, a conclusão bem-sucedida desse método alterará o status de proteção para 0 (proteção desativada), pois, por definição, um volume parcialmente criptografado não será protegido.

## <a name="remarks"></a>Comentários

Se o volume ainda não tiver sido totalmente descriptografado, a execução de **Decrypt** fará com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a descriptografia é o progresso e mostra a porcentagem do volume que permanece criptografado.

Se o status de proteção do volume for "on" antes que esse método seja executado, a execução desse método alterará o status de proteção para "desativado", pois, por definição, um volume parcialmente criptografado não será protegido.

Se esse método for executado no volume do sistema operacional em execução no momento e esse volume do sistema operacional estiver sendo usado para desbloquear automaticamente os volumes de dados (consulte o método [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), você deverá primeiro chamar o método [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]<br/>                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>InfoCard. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
