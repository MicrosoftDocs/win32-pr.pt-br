---
description: Grava a chave externa associada ao protetor de chave de volume especificado em um arquivo de sistema, oculto e somente leitura na pasta especificada.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Método SaveExternalKeyToFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 02269d2b2339ebc8a2b6022bc5f02e63710d496e768be09dad9993c177ed5de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004284"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Método SaveExternalKeyToFile da classe Win32 \_ EncryptableVolume

O método **SaveExternalKeyToFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) grava a chave externa associada ao protetor de chave de volume especificado em um arquivo de sistema, oculto e somente leitura na pasta especificada.

Esse método só é aplicável a protetores de chave do tipo "chave externa" ou "TPM e chave de inicialização".

## <a name="syntax"></a>Sintaxe


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*Caminho* \[ do no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que contém o local do volume ou da pasta onde a chave externa associada ao protetor de chave especificado deve ser salva. Esse caminho não inclui o nome do arquivo, que é interno e pode ser alterado de versão para versão. Use **GetExternalKeyFileName** para obter o nome do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                   | Descrição                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | O volume está bloqueado.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "chave externa" ou "TPM e chave de inicialização".<br/>            |
| <dl> <dt>**Erro \_ do CAMINHO \_ não \_ encontrado**</dt> <dt>2147942403 (0x80070003)</dt> </dl> | O parâmetro *path* não se refere a um local válido.<br/> Verifique se o nome do arquivo não está incluído no parâmetro *path* .<br/> |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                      |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Enterprise, \[ somente aplicativos de área de trabalho do vista Ultimate Windows\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
