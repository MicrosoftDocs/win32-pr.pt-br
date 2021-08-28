---
description: Importa certificados de um arquivo para o armazenamento.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Método Store.Load
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
ms.openlocfilehash: 1b39c2be625ff88869d27e6210e49496352af868c73557d2657c509fd0e79f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897786"
---
# <a name="storeload-method"></a>Método Store.Load

\[O **método** Load está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método Load** importa certificados de um arquivo para o armazenamento.

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

*FileName* \[ Em\]
</dt> <dd>

A cadeia de caracteres que contém o caminho para um arquivo .cer, .sst, .spc, .p7s ou .pfx ou qualquer arquivo assinado authenticode.

</dd> <dt>

*Senha* \[ in, opcional\]
</dt> <dd>

A cadeia de caracteres que contém a senha de texto não criptografado para o arquivo. Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha. Para obter informações sobre como proteger a senha, consulte [Tratamento de senhas](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ in, opcional\]
</dt> <dd>

Um valor da enumeração [**CAPICOM \_ KEY \_ STORAGE \_ FLAG**](capicom-key-storage-flag.md) que define os sinalizadores de armazenamento de chaves. O padrão é CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**PADRÃO DE ARMAZENAMENTO DE CHAVES CAPICOM \_ \_ \_**</dt> </dl>                       | Armazenamento de chaves padrão.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**ARMAZENAMENTO DE CHAVES CAPICOM \_ \_ \_ EXPORTÁVEL**</dt> </dl>              | A chave é exportável.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**USUÁRIO DE ARMAZENAMENTO DE CHAVES CAPICOM \_ \_ \_ \_ PROTEGIDO**</dt> </dl> | A chave é protegida pelo usuário.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o **método Load** for chamado em um armazenamento de memória, todos os contêineres de chave criados serão excluídos quando o armazenamento de memória for excluído. Por exemplo, se um arquivo .pfx for carregado em um armazenamento de memória e posteriormente adicionado a um armazenamento do sistema (como o Meu armazenamento) do armazenamento de memória, o certificado no Meu armazenamento não conterá uma chave. Nesse caso, o arquivo .pfx deve ser carregado diretamente no Meu armazenamento.

Esse método gera CAPICOM E NOT ALLOWED quando ele é baseado em \_ script de um aplicativo baseado na \_ \_ Web.

Se a senha não conseguir descriptografar o arquivo de chave privada, o CSP [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia) padrão deverá ser consultado. Se o CSP padrão for o Provedor de Criptografia Base da Microsoft e a operação de descriptografia falhar, a operação de descriptografia deverá ser tentada novamente com o Provedor de Criptografia Forte da Microsoft ou o Provedor de Criptografia Aprimorado da Microsoft, o que estiver disponível.

Se o certificado que está sendo carregado no armazenamento for o mesmo que aquele que já está lá, o método **Load** excluirá o certificado existente do armazenamento e adicionará o novo certificado. O novo certificado herdará propriedades do certificado existente. O contêiner de chave privada existente é substituído pelo novo contêiner de chave privada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
