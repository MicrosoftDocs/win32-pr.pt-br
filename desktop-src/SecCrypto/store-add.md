---
description: Adiciona um objeto Certificate a um armazenamento de certificados aberto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Método Store.Add
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
ms.openlocfilehash: f90d95184fd789530831628cb6e121e32ce258d4541769c47926d2fb46eb710c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897931"
---
# <a name="storeadd-method"></a>Método Store.Add

\[O **método** Add está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método Add** adiciona um objeto [**Certificate**](certificate.md) a um armazenamento [*de certificados aberto.*](../secgloss/c-gly.md) Esse método só pode ser usado com um armazenamento que foi aberto com permissão de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Certificado* \[ Em\]
</dt> <dd>

Expressão que é resolvida para um [**objeto Certificate**](certificate.md) a ser adicionado ao armazenamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado em um armazenamento do sistema de um script Web, o script precisa acessar certificados digitais no computador local. Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também terá acesso a quaisquer informações pessoais armazenadas nos certificados. Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido.

 

Se o armazenamento não estiver aberto no modo de leitura/gravação, esse método falhará. Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um armazenamento de memória não são persistentes quando o armazenamento é fechado.

Se o certificado que está sendo adicionado ao armazenamento for o mesmo que aquele que já está lá, o método **Add** excluirá o certificado existente do armazenamento e adicionará o novo certificado. O novo certificado herda propriedades do certificado existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
