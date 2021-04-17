---
title: Método Network. setProxySettings
description: O método setProxySettings especifica a configuração de proxy para um determinado protocolo.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- método setProxySettings Windows Media Player
- método setProxySettings Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763205"
---
# <a name="networksetproxysettings-method"></a>Método Network. setProxySettings

O método **setProxySettings** especifica a configuração de proxy para um determinado protocolo.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> <dt>

*configuração* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém um dos valores a seguir.



| Valor | Descrição                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Não use um servidor proxy.                                           |
| 1     | Use as configurações de proxy do navegador atual (válido somente para HTTP). |
| 2     | Use as configurações de proxy especificadas manualmente.                           |
| 3     | Detectar automaticamente as configurações de proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa JScript com um elemento HTML SELECT **para permitir que o usuário especifique a configuração de proxy do Windows Media Player para o protocolo http. O objeto de jogador** foi criado com ID = "Player".


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

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

 

 





