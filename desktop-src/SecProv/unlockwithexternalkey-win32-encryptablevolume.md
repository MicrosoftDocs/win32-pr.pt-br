---
description: Usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Método UnlockWithExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749456"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithExternalKey da classe Win32 \_ EncryptableVolume

O método **UnlockWithExternalKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.

A chave de criptografia do volume deve ter sido protegida com um ou mais protetores de chave do tipo "chave externa" usando o método [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para poder desbloquear o volume com esse método.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExternalKey* \[ no\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume. Essa chave pode ser obtida chamando o método [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se o volume já estiver desbloqueado, esse método retornará 0.



| Código/valor de retorno                                                                                                                                                                  | Descrição                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                                                       |
| <dl> <dt>**Erro \_ do Não \_ encontrado**</dt> <dt>nenhum valor fornecido (0x)</dt> </dl>          | O volume não tem um protetor de chave do tipo "chave externa".<br/>                                                             |
| <dl> <dt>**Erro \_ do \_Senha inválida**</dt> <dt>nenhum valor fornecido (0x)</dt> </dl>   | Existe um ou mais protetores de chave do tipo "chave externa", mas o parâmetro *ExternalKey* especificado não pode desbloquear o volume.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O parâmetro *ExternalKey* não é uma matriz de tamanho 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                |



 

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

 

 
