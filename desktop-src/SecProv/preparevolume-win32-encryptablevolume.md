---
description: Cria um volume do BitLocker com o tipo de sistema de arquivos especificado do volume de descoberta.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Método PrepareVolume da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 67b36703883825d4144037c54ffb55c00308ed1cfb8ee3e4b074d75d63bf7390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891542"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Método PrepareVolume da classe Win32 \_ EncryptableVolume

O método **PrepareVolume** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) cria um volume do BitLocker com o tipo de sistema de arquivos especificado do volume de descoberta. Esse método deve ser chamado antes que o volume possa ser protegido com qualquer um dos métodos **ProtectKeyWith \*** .

## <a name="syntax"></a>Sintaxe

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DiscoveryVolumeType* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica o tipo de volume de descoberta.

| Valor               | Significado                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;None&gt;**    | Nenhum volume de descoberta. Esse valor cria um volume do BitLocker nativo. |
| **&lt;os&gt;** | Esse valor é o comportamento padrão.                                |
| **FAT32**           | Esse valor cria um volume de descoberta FAT32.                       |

</dd> <dt>

*ForceEncryptionType* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Inteiro que especifica o tipo de criptografia. Isso pode ser um dos valores a seguir.

| Valor                                                                                                                                                                                                                                       | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Não especificado**</dt> <dt>0</dt> </dl> | O tipo de criptografia não foi especificado.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Criptografia de software.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Criptografia de hardware.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

| Código/valor de retorno      | Descrição                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | O método foi bem-sucedido.<br/> |

## <a name="remarks"></a>Comentários

Se você não chamar esse método ao habilitar um volume do BitLocker, ele será o mesmo que chamar esse método com o valor padrão no parâmetro *DiscoveryVolumeType* .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise, \[ somente os aplicativos de área de trabalho do Windows 7 Ultimate\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |

## <a name="see-also"></a>Confira também

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
