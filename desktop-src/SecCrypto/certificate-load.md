---
description: Importa um certificado de um arquivo.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'Método ICertificate2:: Load'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fceb6ba9a9868711aefae64865c08e49551e20e8a05686e1691f390f05b76071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771522"
---
# <a name="icertificate2load-method"></a>Método ICertificate2:: Load

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Load** importa um certificado de um arquivo. Esse método foi introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém o caminho para um arquivo. cer ou. pfx que contém os dados do certificado.

</dd> <dt>

*Senha* \[ do em, opcional\]
</dt> <dd>

Uma cadeia de caracteres que contém a senha de [*texto sem formatação*](../secgloss/p-gly.md) para o arquivo de [*chave privada*](../secgloss/p-gly.md) . A senha pode conter até 32 caracteres Unicode, incluindo um caractere nulo de terminação. Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ \_ sinalizador de armazenamento de chave capicor**](capicom-key-storage-flag.md) que define os sinalizadores de armazenamento de chaves. O padrão é o padrão de armazenamento de chave CAPICOM \_ \_ \_ . A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**\_padrão de \_ armazenamento de chave CAPICOM \_**</dt> </dl>                       | Armazenamento de chaves padrão.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**o armazenamento de chaves capicor é \_ \_ \_ exportável**</dt> </dl>              | A chave é exportável.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM de \_ armazenamento de chave \_ \_ \_ protegido pelo usuário**</dt> </dl> | A chave é protegida pelo usuário.<br/> |



 

</dd> <dt>

*Keylocation* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ local da chave CAPICOM**](capicom-key-location.md) que define os tipos de local de chave. O valor padrão é capicor a \_ \_ chave de usuário atual \_ . A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                               | Significado                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**CAPICOM da \_ \_ chave de usuário atual \_**</dt> </dl>    | A chave é uma chave de usuário.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**\_chave do \_ computador \_ local CAPICOM**</dt> </dl> | A chave é uma chave de computador.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
