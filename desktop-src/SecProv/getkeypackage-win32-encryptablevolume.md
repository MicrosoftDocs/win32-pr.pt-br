---
description: Exporta informações que podem ajudar a recuperar dados criptografados quando a unidade está gravemente danificada e nenhum arquivo de backup de dados existe.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Método GetKeyPackage da Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 777c68bab142fc0f27d9200d2aea1ff0c45c47181d951600dcc96bb0e623b6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892353"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyPackage da classe EncryptableVolume do Win32 \_

O **método GetKeyPackage** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exporta informações que podem ajudar a recuperar dados criptografados quando a unidade está gravemente danificada e não existem arquivos de backup de dados.

As informações exportadas consistem na chave de criptografia do volume protegida por um protetor de chave do tipo "Senha Numérica" ou "Chave Externa". Para usar esse pacote, você também deve salvar a senha numérica ou a chave externa correspondente.

> [!IMPORTANT]
> Se você optar por exportar um pacote de chaves, certifique-se de manter essas informações em um local bem protegido. Não carregue essas informações com seu computador. Se esse pacote de chaves for perdido ou roubado, você precisará descriptografar o volume e recriptá-lo usando uma nova chave.

 

No caso de uma falha de unidade, a Ferramenta de Reparo do BitLocker existe para ajudar a recuperar os dados disponíveis. Para obter mais informações sobre como essa ferramenta pode usar o pacote de chaves, consulte Como usar a Ferramenta de Reparo do [BitLocker](https://support.microsoft.com/kb/928201)para ajudar a recuperar dados de um volume criptografado no Windows Vista .

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado. Para exportar um pacote de chaves, você deve usar um protetor de chave do tipo "Senha Numérica" ou "Chave Externa".

</dd> <dt>

*KeyPackage \[ \]* \[out\]
</dt> <dd>

Tipo: **uint8**

Um fluxo de byte que contém a chave de criptografia para um volume, protegido pelo protetor de chave especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | O volume está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PROTECTOR NÃO ENCONTRADO \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | O protetor de chave fornecido não existe no volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ TIPO DE PROTETOR \_ \_ INVÁLIDO**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | O *parâmetro VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "Senha Numérica" ou "Chave Externa". Use o [**método ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar um protetor de chave do tipo apropriado.<br/> |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Windows SDK. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
