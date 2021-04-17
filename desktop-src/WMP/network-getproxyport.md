---
title: Método Network. getProxyPort
description: O método getProxyPort recupera a porta do proxy que está sendo usada.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- método getProxyPort Windows Media Player
- método getProxyPort Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763030"
---
# <a name="networkgetproxyport-method"></a>Método Network. getProxyPort

O método **getProxyPort** recupera a porta do proxy que está sendo usada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Network.getProxyPort(
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

Esse método retorna um **número** (**longo**) que contém a porta do proxy que está sendo usada. O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).

## <a name="remarks"></a>Comentários

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **getProxyPort** para exibir os números de porta do proxy do Windows Media Player atuais para os protocolos MMS e http. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

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

 

 





