---
title: Cancelar registro do IAgent
description: Cancelar registro do IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823761"
---
# <a name="iagentunregister"></a>IAgent:: cancelar registro

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 