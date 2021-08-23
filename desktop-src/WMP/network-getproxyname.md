---
title: Método Network.getProxyName
description: O método getProxyName recupera o nome do servidor proxy que está sendo usado.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- Método getProxyName Windows Media Player
- Método getProxyName Windows Media Player , Classe de rede
- Classe de Windows Media Player , método getProxyName
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f40eb7eb695376768cd8168e1eb1d1916c8e84e6ede8ef93251df6097a15d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647446"
---
# <a name="networkgetproxyname-method"></a>Método Network.getProxyName

O **método getProxyName** recupera o nome do servidor proxy que está sendo usado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que especifica o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma **Cadeia de** caracteres que contém o nome do servidor proxy que está sendo usado. O valor retornado é significativo somente **quando getProxySettings** retorna um valor de 2 (use configurações manuais).

## <a name="remarks"></a>Comentários

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *Rede*. **getProxyName para** exibir os nomes Windows Media Player do servidor proxy para os protocolos HTTP e MMS. O **objeto** Player foi criado com ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Network.getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





