---
title: Método Network.setProxyExceptionList
description: O método setProxyExceptionList especifica a lista de exceções de proxy. | Método Network.setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- Método setProxyExceptionList Windows Media Player
- Método setProxyExceptionList Windows Media Player , classe network
- Classe de Windows Media Player , método setProxyExceptionList
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
ms.openlocfilehash: cf72d9c35778e965021ec31671e4e345ec2d8e281d18f9fcb16c8f2ff04d4722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647296"
---
# <a name="networksetproxyexceptionlist-method"></a>Método Network.setProxyExceptionList

O **método setProxyExceptionList** especifica a lista de exceções de proxy.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que especifica o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> <dt>

*lista* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que especifica uma lista delimitada por ponto e vírgula de hosts para os quais o servidor proxy é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esta é uma lista de computadores, domínios e/ou endereços que ignorarão o servidor proxy quando a parte do host da URL de destino corresponde a uma entrada na lista.

O \* caractere pode ser usado como um curinga para listar entradas. Por exemplo, .com corresponderia a todos os hosts no domínio com, enquanto 67. corresponderia a todos os hosts na \* sub-rede A da classe \* 67.

Esse método não tem efeito, a **menos que getProxySettings** retorne um valor de 2 (use configurações manuais).

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *Rede*. **setProxyExceptionList para** especificar uma lista de hosts para os quais o servidor proxy é ignorado ao usar o protocolo MMS. A nova lista é recuperada de um elemento HTML TEXT com ID = "XLIST". O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





