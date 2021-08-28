---
title: Método Network.setProxyBypassForLocal
description: O método setProxyBypassForLocal especifica um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- Método setProxyBypassForLocal Windows Media Player
- Método setProxyBypassForLocal Windows Media Player classe , Network
- Classe de Windows Media Player , método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f0b975ea1f4ddade347205b627c13a708ad33d2132cf2990075c034957f071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836228"
---
# <a name="networksetproxybypassforlocal-method"></a>Método Network.setProxyBypassForLocal

O **método setProxyBypassForLocal** especifica um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que especifica o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> <dt>

*bypass* \[ Em\]
</dt> <dd>

**Booliana** especificando se o servidor proxy é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não tem efeito, a **menos que getProxySettings** retorne um valor de 2 (use configurações manuais).

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Rede*. **setProxyBypassForLocal** para especificar se o servidor proxy Windows Media Player é ignorado, ao usar o protocolo MMS, se o servidor de origem estiver em uma rede local. O **objeto** Player foi criado com ID = "Player".


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
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

 

 





