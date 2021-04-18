---
title: Método Network. setproxyname
description: O método setproxyname especifica o nome do servidor proxy a ser usado. | Método Network. setproxyname
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- método setproxyname do Windows Media Player
- método setproxyname Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setproxyname
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788885"
---
# <a name="networksetproxyname-method"></a>Método Network. setproxyname

O método **Setproxyname** especifica o nome do servidor proxy a ser usado.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do servidor proxy a ser usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **Setproxyname** para especificar o nome do servidor proxy do Windows Media Player para o protocolo MMS. O novo nome é recuperado de um elemento de texto HTML com ID = "NAME". O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
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

 

 





