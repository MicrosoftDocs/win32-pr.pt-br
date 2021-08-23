---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e4f3fe070a944ecd9800a6712e8ae4db8d333913e5cfe85c027565cf1cf77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609376"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::GetHotKey

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Endereço de um BSTR que recebe a configuração de tecla de atalho atual usada para abrir o canal de áudio para entrada de fala.

</dd> </dl>

Se [**GetEnabled**](iagentspeechinputproperties--getenabled.md) retornar **False,** a consulta dessa configuração gera um erro.

## <a name="see-also"></a>Consulte Também

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




