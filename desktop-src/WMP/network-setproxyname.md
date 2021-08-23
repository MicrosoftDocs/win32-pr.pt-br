---
title: Método Network.setProxyName
description: O método setProxyName especifica o nome do servidor proxy a ser usado. | Método Network.setProxyName
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- Método setProxyName Windows Media Player
- Método setProxyName Windows Media Player , Classe de rede
- Classe de Windows Media Player , método setProxyName
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
ms.openlocfilehash: 9831b25e37fd6e19b70c1ee2589736394560c97f841b5d18c3a128a82997cc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134919"
---
# <a name="networksetproxyname-method"></a>Método Network.setProxyName

O **método setProxyName** especifica o nome do servidor proxy a ser usado.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que especifica o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> <dt>

*name* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que especifica o nome do servidor proxy a ser usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não tem efeito, a **menos que getProxySettings** retorne um valor de 2 (use configurações manuais).

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *Rede*. **setProxyName** para especificar o nome do servidor proxy Windows Media Player para o protocolo MMS. O novo nome é recuperado de um elemento HTML TEXT com ID = "NAME". O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





