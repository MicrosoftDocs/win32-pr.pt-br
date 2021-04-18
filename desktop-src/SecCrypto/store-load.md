---
description: Importa certificados de um arquivo para o repositório.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Método Store. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783227"
---
# <a name="storeload-method"></a>Método Store. Load

\[O método **Load** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Load** importa certificados de um arquivo para o repositório.

## <a name="syntax"></a>Sintaxe


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

A cadeia de caracteres que contém o caminho para um arquivo. cer,. SST,. SPC,. p7s ou. pfx ou qualquer arquivo assinado por Authenticode.

</dd> <dt>

*Senha* \[ do em, opcional\]
</dt> <dd>

A cadeia de caracteres que contém a senha de texto sem formatação para o arquivo. Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha. Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ \_ sinalizador de armazenamento de chave capicor**](capicom-key-storage-flag.md) que define os sinalizadores de armazenamento de chaves. O padrão é o padrão de armazenamento de chave CAPICOM \_ \_ \_ . Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**\_padrão de \_ armazenamento de chave CAPICOM \_**</dt> </dl>                       | Armazenamento de chaves padrão.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**o armazenamento de chaves capicor é \_ \_ \_ exportável**</dt> </dl>              | A chave é exportável.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM de \_ armazenamento de chave \_ \_ \_ protegido pelo usuário**</dt> </dl> | A chave é protegida pelo usuário.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método **Load** for chamado em um repositório de memória, os contêineres de chave criados serão excluídos quando o armazenamento de memória for excluído. Por exemplo, se um arquivo. pfx for carregado em um repositório de memória e adicionado posteriormente a um repositório do sistema (como o meu repositório) do armazenamento de memória, o certificado no meu repositório não conterá uma chave. Nesse caso, o arquivo. pfx deve ser carregado diretamente no meu repositório.

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

Se a senha falhar ao descriptografar o arquivo de chave privada, o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) padrão deverá ser consultado. Se o CSP padrão for o provedor criptográfico base da Microsoft e a operação de descriptografia falhar, a operação de descriptografia deverá ser tentada novamente com o provedor de criptografia forte da Microsoft ou com o provedor criptográfico avançado da Microsoft, o que estiver disponível.

Se o certificado que está sendo carregado no repositório for o mesmo que já existe, o método **Load** excluirá o certificado existente do repositório e, em seguida, adicionará o novo certificado. O novo certificado herdará as propriedades do certificado existente. O contêiner de chave privada existente é substituído pelo novo contêiner de chave privada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> </dl>

 

 
