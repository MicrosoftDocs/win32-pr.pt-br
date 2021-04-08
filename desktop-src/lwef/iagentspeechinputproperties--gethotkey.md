---
title: IAgentSpeechInputProperties gettecla de atalho
description: IAgentSpeechInputProperties gettecla de atalho
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004783"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Recupera a atribuição de teclado atual para a chave de escuta de entrada de fala.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

Endereço de um BSTR que recebe a configuração de atalho atual usada para abrir o canal de áudio para entrada de fala.

</dd> </dl>

Se [**Getabilited**](iagentspeechinputproperties--getenabled.md) retornar **false**, a consulta dessa configuração gerará um erro.

## <a name="see-also"></a>Consulte Também

[**IAgentSpeechInputProperties:: getabilited**](iagentspeechinputproperties--getenabled.md)


 

 




