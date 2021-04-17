---
description: Adiciona um objeto de certificado a um repositório de certificados aberto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Método Store. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768427"
---
# <a name="storeadd-method"></a>Método Store. Add

\[O método **Add** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Add** adiciona um objeto de [**certificado**](certificate.md) a um [*repositório de certificados*](../secgloss/c-gly.md)aberto. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Certificado* \[ do no\]
</dt> <dd>

Expressão que resolve para um objeto de [**certificado**](certificate.md) a ser adicionado ao repositório.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado em um repositório de sistema de um script da Web, o script precisa acessar certificados digitais no computador local. Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também obterá acesso a todas as informações pessoais armazenadas nos certificados. Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido.

 

Se o repositório não estiver aberto no modo de leitura/gravação, esse método falhará. Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um repositório de memória não são mantidas quando o armazenamento é fechado.

Se o certificado que está sendo adicionado ao repositório for o mesmo que já existe, o método **Add** excluirá o certificado existente da loja e, em seguida, adicionará o novo certificado. O novo certificado herda as propriedades do certificado existente.

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

 

 
