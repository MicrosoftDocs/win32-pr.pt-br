---
title: Cancelar registro do IAgent
description: Cancelar registro do IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101d0473e8563e8b0899e2f5d0bd2a440c31d17b4a0c142b43f47855ddf166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976476"
---
# <a name="iagentunregister"></a>IAgent:: cancelar registro

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Descarrega os dados de caractere do caractere especificado da coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

A ID do coletor de notificação.

</dd> </dl>

Use esse método quando não precisar mais dos serviços do Microsoft Agent, como quando o aplicativo for desligado.

## <a name="see-also"></a>Consulte Também

[**IAgent:: Register**](iagent--register.md)


 

 