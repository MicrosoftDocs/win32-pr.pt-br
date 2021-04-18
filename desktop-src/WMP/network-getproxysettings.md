---
title: Método Network. getProxySettings
description: O método getProxySettings recupera a configuração de proxy para um determinado protocolo.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- método getProxySettings Windows Media Player
- método getProxySettings Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751373"
---
# <a name="networkgetproxysettings-method"></a>Método Network. getProxySettings

O método **getProxySettings** recupera a configuração de proxy para um determinado protocolo.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Network.getProxySettings(
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

Esse método retorna um **número** (**Long**) contendo um dos valores a seguir.



| Valor | Descrição                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Um servidor proxy não está sendo usado.                                                |
| 1     | As configurações de proxy para o navegador atual estão sendo usadas (válida somente para HTTP). |
| 2     | As configurações de proxy especificadas manualmente estão sendo usadas.                            |
| 3     | As configurações de proxy estão sendo detectadas automaticamente.                                      |



 

## <a name="remarks"></a>Comentários

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **getProxySettings** para exibir uma mensagem, que fornece informações sobre as configurações de proxy atuais do Player, na janela do navegador. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

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

 

 





