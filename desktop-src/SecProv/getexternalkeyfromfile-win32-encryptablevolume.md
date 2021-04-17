---
description: Retorna a chave externa de um arquivo.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Método GetExternalKeyFromFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761851"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Método GetExternalKeyFromFile da classe Win32 \_ EncryptableVolume

O método **GetExternalKeyFromFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retorna a chave externa de um arquivo criado pelo [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), dado o local desse arquivo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PathWithFileName* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica o local do arquivo que contém uma chave externa.

</dd> <dt>

*ExternalKey* \[ fora\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de bytes que é a chave externa de 256 bits contida no arquivo que pode ser usada para desbloquear um volume.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                   | Descrição                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | O método foi bem-sucedido.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | O arquivo não contém uma chave externa.<br/>  |
| <dl> <dt>**Erro \_ do ARQUIVO \_ não \_ encontrado**</dt> <dt>2147942402 (0x80070002)</dt> </dl> | Não é possível localizar o arquivo no local especificado.<br/> |



 

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

 

 
