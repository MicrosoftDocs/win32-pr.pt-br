---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105797908"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Recupera um valor que indica se a dica de escuta está habilitada para exibição.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Endereço de uma variável que recebe **true** se a dica de escuta estiver habilitada para exibição ou **false** se a dica de escuta estiver desabilitada.

</dd> </dl>

Se [**Getabilited**](iagentspeechinputproperties--getenabled.md) retornar **false**, a consulta de qualquer outra propriedade de entrada de fala retornará um erro.

## <a name="see-also"></a>Consulte Também

[**IAgentSpeechInputProperties:: getabilited**](iagentspeechinputproperties--getenabled.md)


 

 




