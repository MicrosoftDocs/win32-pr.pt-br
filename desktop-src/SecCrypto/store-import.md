---
description: O método de importação copia para um certificado aberto armazena o conteúdo de um repositório de certificados exportado anteriormente. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Método Store. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747232"
---
# <a name="storeimport-method"></a>Método Store. Import

\[O método de **importação** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método de **importação** copia para um [*certificado aberto armazena*](../secgloss/c-gly.md) o conteúdo de um repositório de certificados exportado anteriormente. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncodedStore* \[ no\]
</dt> <dd>

A cadeia de caracteres que contém os certificados codificados a serem importados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado de um script da Web, o script precisa acessar certificados digitais no computador local. Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também obterá acesso a todas as informações pessoais armazenadas nos certificados. Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido.

 

Se o repositório não estiver aberto com permissão de leitura/gravação, esse método falhará. Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um repositório de memória não são mantidas quando o armazenamento é fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
