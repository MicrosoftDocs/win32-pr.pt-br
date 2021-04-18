---
title: Método Network. setProxyPort
description: O método setProxyPort especifica a porta proxy a ser usada. | Método Network. setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- método setProxyPort Windows Media Player
- método setProxyPort Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794616"
---
# <a name="networksetproxyport-method"></a>Método Network. setProxyPort

O método **setProxyPort** especifica a porta proxy a ser usada.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> <dt>

*porta* \[ do no\]
</dt> <dd>

**Número** (**longo**) que especifica a porta do proxy a ser usada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **setProxyPort** para especificar o número da porta do proxy do Windows Media Player para o protocolo MMS. O número da porta é recuperado de um elemento de entrada HTML com ID = "PORT". O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
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

 

 





