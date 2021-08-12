---
title: Método Network.setProxySettings
description: O método setProxySettings especifica a configuração de proxy para um determinado protocolo.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- Método setProxySettings Windows Media Player
- Método setProxySettings Windows Media Player , Classe de rede
- Classe de Windows Media Player , método setProxySettings
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
ms.openlocfilehash: 6501d097a4ec342c2831e4b72bf8f17edc4e4e1bec02b2b51cd7840325674b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573854"
---
# <a name="networksetproxysettings-method"></a>Método Network.setProxySettings

O **método setProxySettings** especifica a configuração de proxy para um determinado protocolo.

## <a name="syntax"></a>Sintaxe


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*protocolo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que especifica o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> <dt>

*configuração* \[ Em\]
</dt> <dd>

**Número** (**longo**) que contém um dos valores a seguir.



| Valor | Descrição                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Não use um servidor proxy.                                           |
| 1     | Use as configurações de proxy do navegador atual (válido somente para HTTP). |
| 2     | Use as configurações de proxy especificadas manualmente.                           |
| 3     | Detecte automaticamente as configurações de proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa JScript com um elemento HTML SELECT para permitir que o usuário especifique a **configuração Windows Media Player proxy para o protocolo HTTP. O objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





