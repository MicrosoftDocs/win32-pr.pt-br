---
title: Método Network. getproxyname
description: O método getproxyname recupera o nome do servidor proxy que está sendo usado.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- método getproxyname do Windows Media Player
- método getproxyname Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getproxyname
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
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771543"
---
# <a name="networkgetproxyname-method"></a>Método Network. getproxyname

O método **Getproxyname** recupera o nome do servidor proxy que está sendo usado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Network.getProxyName(
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

Esse método retorna uma **cadeia de caracteres** que contém o nome do servidor proxy que está sendo usado. O valor retornado é significativo somente quando **getProxySettings** retorna um valor de 2 (use configurações manuais).

## <a name="remarks"></a>Comentários

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **Getproxyname** para exibir os nomes do servidor proxy do Windows Media Player para os protocolos http e MMS. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Network. getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





