---
description: Indica o status da criptografia ou descriptografia no volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Método GetConversionStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826975"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetConversionStatus da classe Win32 \_ EncryptableVolume

O método **GetConversionStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica o status da criptografia ou descriptografia no volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConversionStatus* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Criptografia de volume ou status de descriptografia. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | Para uma HDD (unidade de disco rígido) padrão, o volume é totalmente descriptografado.<br/> Para um disco rígido criptografado por hardware (EHDD), o volume é permanente desbloqueado.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | Para uma HDD (unidade de disco rígido) padrão, o volume é totalmente criptografado.<br/> Para um disco rígido criptografado por hardware (EHDD), o volume não é permanente desbloqueado.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | O volume é parcialmente criptografado.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | O volume é parcialmente criptografado.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | O volume foi pausado durante o andamento da criptografia. O volume é parcialmente criptografado.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | O volume foi pausado durante o andamento da descriptografia. O volume é parcialmente criptografado.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Porcentagem do volume que é criptografado. Este é um inteiro de 0 a 100, inclusive.

Devido ao arredondamento de números, um percentual de criptografia de 0 ou 100 não indica necessariamente que o disco está totalmente descriptografado ou totalmente criptografado. Sempre use *ConversionStatus* para determinar se o disco está, de fato, totalmente descriptografado ou totalmente criptografado.

</dd> <dt>

*EncryptionFlags* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Sinalizadores que descrevem o comportamento de criptografia.

Uma combinação de 32 bits com os seguintes bits definidos no momento.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia. Se a criptografia tiver sido pausada ou interrompida, chamar o método [**Encrypt**](encrypt-win32-encryptablevolume.md) efetivamente retomará a conversão e o valor desse bit será ignorado. Esse bit só tem efeito quando os métodos **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) iniciam a criptografia do estado totalmente descriptografado, a descriptografia em estado de andamento ou o status de descriptografia em pausa. Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Execute o apagamento sob demanda do espaço livre no volume. A chamada do método [**Encrypt**](encrypt-win32-encryptablevolume.md) com esse conjunto de bits só é permitida quando o volume não está convertendo ou apagando e está em um estado "criptografado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Execute a operação solicitada de forma síncrona. A chamada será bloqueada até que a operação solicitada seja concluída ou interrompida. Só há suporte para esse sinalizador com o método [**Encrypt**](encrypt-win32-encryptablevolume.md) . Esse sinalizador pode ser **especificado quando a criptografia é** chamada para retomar a criptografia interrompida ou interrompida ou apagar ou quando a criptografia ou o apagamento estiver em andamento. Isso permite que o chamador retome de forma síncrona aguardando até que o processo seja concluído ou interrompido.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Status de apagamento de espaço livre. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                               | Significado                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | O espaço livre não foi apagado.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | O espaço livre foi apagado.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | O apagamento de espaço livre está em andamento no momento.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | O apagamento de espaço livre foi pausado.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Um valor de 0 a 100 que especifica a porcentagem de espaço livre que foi apagado.

</dd> <dt>

*PrecisionFactor* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Um valor de 0 a 4 que especifica o nível de precisão

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                  | Descrição                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>      |



 

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

 

 
