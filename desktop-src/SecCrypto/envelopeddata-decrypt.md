---
description: Descriptografa o conteúdo Envelopado.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Método EnvelopedData. Decrypt
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
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752336"
---
# <a name="envelopeddatadecrypt-method"></a>Método EnvelopedData. Decrypt

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Decrypt** descriptografa o conteúdo Envelopado. A descriptografia é feita se o destinatário da mensagem tiver acesso à [*chave privada*](../secgloss/p-gly.md) emparelhada com uma das [*chaves públicas*](../secgloss/p-gly.md) usadas para envelope a mensagem. Chamar o método **decodificar** redefine o [*estado*](../secgloss/s-gly.md) do objeto. Se o método **Decrypt** for executado com sucesso, a propriedade [**Content**](envelopeddata-content.md) do objeto [**EnvelopedData**](envelopeddata.md) será definida como a mensagem de texto sem formatação.

## <a name="syntax"></a>Sintaxe


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnvelopedMessage* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém os dados de envelope a serem descriptografados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os dados descriptografados se tornam o valor da propriedade [**Content**](envelopeddata-content.md) para o objeto [**EnvelopedData**](envelopeddata.md) .

Se o usuário desse método não tiver acesso a uma chave privada que corresponda a uma das chaves públicas usadas para envelope a mensagem, o método falhará. Esse método falhará se o certificado da chave privada associada não estiver no computador local MY Store ou no usuário atual MY Store.

> [!IMPORTANT]
> Quando esse método é chamado de um script da Web, o script precisa usar sua [*chave privada*](../secgloss/p-gly.md) para descriptografar os dados. Permitir que sites não confiáveis usem sua chave privada é um risco de segurança. Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez. Se você permitir que o script Use sua chave privada e selecionar "não perguntar novamente", a caixa de diálogo não aparecerá mais para nenhum script que use sua chave privada para descriptografar os dados dentro desse domínio. No entanto, os scripts fora desse domínio que tentarem usar sua chave privada para descriptografar dados ainda farão com que essa caixa de diálogo seja exibida. Se você não permitir que o script Use sua chave privada e selecionar "não perguntar novamente", os scripts nesse domínio serão recusados automaticamente a capacidade de usar sua chave privada para descriptografar os dados.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
