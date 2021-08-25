---
description: Descriptografa o conteúdo envelhado.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Método EnvelopedData.Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f1c754e23977ac9c7af7f4fd3feaade13c928e9522a2285102a095fff4740b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874256"
---
# <a name="envelopeddatadecrypt-method"></a>Método EnvelopedData.Decrypt

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use [**a Classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

O **método Decrypt** descriptografa o conteúdo envelhado. A descriptografia será feita se o destinatário [](../secgloss/p-gly.md) da mensagem tiver acesso [](../secgloss/p-gly.md) à chave privada emparelhada com uma das chaves públicas usadas para envolver a mensagem. Chamar o **método Decrypt** redefine [*o estado*](../secgloss/s-gly.md) do objeto . Se o **método Decrypt** for bem-sucedido, a propriedade [**Content**](envelopeddata-content.md) do [**objeto EnvelopedData**](envelopeddata.md) será definida como a mensagem de texto não criptografado.

## <a name="syntax"></a>Sintaxe


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnvelopedMessage* \[ Em\]
</dt> <dd>

Cadeia de caracteres que contém os dados envelhados a serem descriptografados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os dados descriptografados se tornam [**o valor da**](envelopeddata-content.md) propriedade Content para o objeto [**EnvelopedData.**](envelopeddata.md)

Se o usuário desse método não tiver acesso a uma chave privada que corresponde a uma das chaves públicas usadas para envolver a mensagem, o método falhará. Esse método falhará se o certificado da chave privada associada não estiver no computador local MY Store ou no usuário atual MY Store.

> [!IMPORTANT]
> Quando esse método é chamado de um script Web, o script precisa usar sua [*chave privada*](../secgloss/p-gly.md) para descriptografar os dados. Permitir que sites não confiáveis usem sua chave privada é um risco de segurança. Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez. Se você permitir que o script use sua chave privada e selecionar "Não me pergunte isso novamente", a caixa de diálogo não será mais exibida para nenhum script que use sua chave privada para descriptografar dados dentro desse domínio. No entanto, scripts fora desse domínio que tentam usar sua chave privada para descriptografar dados ainda fará com que essa caixa de diálogo apareça. Se você não permitir que o script use sua chave privada e selecionar "Não perguntar isso novamente", os scripts dentro desse domínio serão recusados automaticamente a capacidade de usar sua chave privada para descriptografar dados.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
