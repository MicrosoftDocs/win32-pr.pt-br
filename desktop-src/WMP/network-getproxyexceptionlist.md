---
title: Método Network. getProxyExceptionList
description: O método getProxyExceptionList recupera a lista de exceções de proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- método getProxyExceptionList Windows Media Player
- método getProxyExceptionList Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772934"
---
# <a name="networkgetproxyexceptionlist-method"></a>Método Network. getProxyExceptionList

O método **getProxyExceptionList** recupera a lista de exceções de proxy.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres** especificando uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado. O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).

## <a name="remarks"></a>Comentários

Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.

O \* caractere pode ser usado como um caractere curinga para listar entradas. Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **getProxyExceptionList** para exibir as listas de proxies ignorados para os protocolos MMS e http. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Network. getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





