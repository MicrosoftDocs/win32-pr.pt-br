---
title: Método Network. getProxyBypassForLocal
description: O método getProxyBypassForLocal recupera um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- método getProxyBypassForLocal Windows Media Player
- método getProxyBypassForLocal Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760542"
---
# <a name="networkgetproxybypassforlocal-method"></a>Método Network. getProxyBypassForLocal

O método **getProxyBypassForLocal** recupera um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Network.getProxyBypassForLocal(
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

Esse método retorna um **valor booleano** que indica se o servidor proxy é ignorado. O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).

## <a name="remarks"></a>Comentários

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **getProxyBypassForLocal** para exibir se o Windows Media Player está definido para ignorar o servidor proxy para endereços locais. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

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

 

 





