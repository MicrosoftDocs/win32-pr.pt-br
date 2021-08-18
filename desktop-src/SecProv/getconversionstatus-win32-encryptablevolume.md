---
description: Indica o status da criptografia ou descriptografia no volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Método GetConversionStatus da classe Win32_EncryptableVolume dados
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
ms.openlocfilehash: a93e52e0df7f4ab3fdc4c4686ee05e9c1bc9c2c3082604d922da56bc57cb94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004475"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetConversionStatus da classe EncryptableVolume do Win32 \_

O **método GetConversionStatus** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) indica o status da criptografia ou descriptografia no volume.

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

*ConversionStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Criptografia de volume ou status de descriptografia. Esse pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | Para um HDD (disco rígido padrão), o volume é totalmente descriptografado.<br/> Para um EHDD (disco rígido criptografado de hardware), o volume é desbloqueado permanentemente.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | Para um HDD (disco rígido padrão), o volume é totalmente criptografado.<br/> Para um EHDD (disco rígido criptografado de hardware), o volume não é desbloqueado permanentemente.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | O volume é parcialmente criptografado.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | O volume é parcialmente criptografado.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | O volume foi pausado durante o progresso da criptografia. O volume é parcialmente criptografado.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | O volume foi pausado durante o progresso da descriptografia. O volume é parcialmente criptografado.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ out\]
</dt> <dd>

Tipo: **uint32**

Percentual do volume que é criptografado. Este é um inteiro de 0 a 100, inclusive.

Devido ao arredondamento de números, um percentual de criptografia de 0 ou 100 não indica necessariamente que o disco está totalmente descriptografado ou totalmente criptografado. Sempre use *ConversionStatus* para determinar se o disco é, na verdade, totalmente descriptografado ou totalmente criptografado.

</dd> <dt>

*EncryptionFlags* \[ out\]
</dt> <dd>

Tipo: **uint32**

Sinalizadores que descrevem o comportamento de criptografia.

Uma combinação de 32 bits com os bits a seguir definidos no momento.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia. Se a criptografia tiver sido pausada ou interrompida, chamar o [**método Encrypt**](encrypt-win32-encryptablevolume.md) retomará efetivamente a conversão e o valor desse bit será ignorado. Esse bit só tem efeito quando os métodos **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) iniciam a criptografia do estado totalmente descriptografado, descriptografia em estado de andamento ou estado em pausa de descriptografia. Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Execute o apagando sob demanda do espaço livre do volume. Chamar o [**método Encrypt**](encrypt-win32-encryptablevolume.md) com esse conjunto de bits só é permitido quando o volume não está convertendo ou apagando no momento e está em um estado "criptografado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Execute a operação solicitada de forma síncrona. A chamada será interrompida até que a operação solicitada seja concluída ou tenha sido interrompida. Esse sinalizador só tem suporte com o [**método Encrypt.**](encrypt-win32-encryptablevolume.md) Esse sinalizador pode ser especificado quando **Encrypt** é chamado para retomar a criptografia interrompida ou interrompida ou apagamento ou quando a criptografia ou a limpeza está em andamento. Isso permite que o chamador retome a espera síncrona até que o processo seja concluído ou interrompido.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Status de apagamento de espaço livre. Esse pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                               | Significado                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | O espaço livre não foi apagado.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | O espaço livre foi apagado.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | A limpeza de espaço livre está em andamento no momento.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | A limpeza de espaço livre foi pausada.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ out\]
</dt> <dd>

Tipo: **uint32**

Um valor de 0 a 100 que especifica o percentual de espaço livre que foi apagado.

</dd> <dt>

*PrecisionFactor* \[ Em\]
</dt> <dd>

Tipo: **uint32**

Um valor de 0 a 4 que especifica o nível de precisão

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                  | Descrição                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>      |



 

## <a name="remarks"></a>Comentários

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

 

 
