---
title: Método Network. getProxyBypassForLocal
description: O método getProxyBypassForLocal recupera um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- Windows Media Player do método getProxyBypassForLocal
- método getProxyBypassForLocal Windows Media Player, classe de rede
- classe de rede Windows Media Player, método getProxyBypassForLocal
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
ms.openlocfilehash: 51f22eb6187938318d95b9dd7a473b58e216315210d4af41c29b352b2654cbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054554"
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

## <a name="return-value"></a>Valor retornado

Esse método retorna um **valor booleano** que indica se o servidor proxy é ignorado. O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).

## <a name="remarks"></a>Comentários

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa a *rede*. **getProxyBypassForLocal** para exibir se Windows Media Player está definido para ignorar o servidor proxy para endereços locais. O objeto de **jogador** foi criado com ID = "Player".


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

 

 





