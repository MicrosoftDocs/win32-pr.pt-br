---
title: Método Network. setProxyExceptionList
description: O método setProxyExceptionList especifica a lista de exceções de proxy. | Método Network. setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- método setProxyExceptionList Windows Media Player
- método setProxyExceptionList Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763838"
---
# <a name="networksetproxyexceptionlist-method"></a>Método Network. setProxyExceptionList

O método **setProxyExceptionList** especifica a lista de exceções de proxy.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> <dt>

*lista* \[ de no\]
</dt> <dd>

**Cadeia de caracteres** que especifica uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.

O \* caractere pode ser usado como um caractere curinga para listar entradas. Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.

Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **setProxyExceptionList** para especificar uma lista de hosts para os quais o servidor proxy é ignorado ao usar o protocolo MMS. A nova lista é recuperada de um elemento de texto HTML com ID = "XLIST". O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





