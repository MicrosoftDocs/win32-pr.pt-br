---
description: O método remove remove um certificado de um repositório de certificados aberto. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Método Store. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f3700c8f61861987bc5311a637722955c62a1c6ad1572c7628d9ab9e0f5c76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897681"
---
# <a name="storeremove-method"></a>Método Store. Remove

\[O método **Remove** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Remove** remove um [*certificado*](../secgloss/c-gly.md) de um [*repositório de certificados*](../secgloss/c-gly.md)aberto. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Certificado* \[ do no\]
</dt> <dd>

Expressão que resolve para uma instância de um objeto de [**certificado**](certificate.md) a ser removido do repositório.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado de um script da Web, o script precisa excluir certificados digitais do computador local. Permitir que sites não confiáveis exclua certificados digitais é um risco de segurança. Uma caixa de diálogo que pergunta se o site pode excluir certificados é exibida quando esse método é chamado pela primeira vez. Se você permitir que o aplicativo exclua certificados e selecionar "não mostrar esta caixa de diálogo novamente", a caixa de diálogo não aparecerá mais para nenhum script que exclua certificados dentro desse domínio. No entanto, os scripts fora desse domínio que tentarem excluir certificados ainda farão com que essa caixa de diálogo seja exibida. Se você não permitir que o script exclua certificados e selecionar "não mostrar esta caixa de diálogo novamente", os scripts nesse domínio serão recusados automaticamente na capacidade de excluir certificados.

 

Ao excluir um certificado de um repositório, primeiro exclua a chave privada associada ao certificado.

Se o armazenamento não estiver aberto com permissão de leitura/gravação, esse método falhará. Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um repositório de memória não são mantidas quando o armazenamento é fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
