---
description: Distribuidores de plug-in
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Distribuidores de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70d253066fdde4f082a964c56a221331cfd127c0984db2a7b1933a0bb352425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583656"
---
# <a name="plug-in-distributors"></a>Distribuidores de plug-in

Os PIDs (distribuidores de plug-in) são uma maneira de estender a funcionalidade do gerenciador de grafo de filtro. Um distribuidor de plug-in é um objeto COM que o gerenciador de grafo de filtro agrega em tempo de operação. Os aplicativos obtém acesso ao PID por meio do gerenciador de grafo de filtro.

Quando o gerenciador de grafo de filtro é consultado para uma interface que não dá suporte, ele pesquisa no Registro uma chave com o seguinte formulário:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` é uma cadeia de caracteres que contém o identificador de interface. Se a entrada do Registro existir, o valor da entrada definirá o CLSID (identificador de classe) de um PID que dá suporte à interface . O gerenciador de grafo de filtro agrega o PID e retorna um ponteiro de interface, atuando assim como **o IUnknown externo** para o PID. Quando o aplicativo chama métodos na interface, ele está realmente chamando-os no PID. No entanto, a existência do PID é transparente para o aplicativo.

O termo *distribuidor* deriva do fato de que um PID pode consultar seu ponteiro **IUnknown** externo para interfaces no gerenciador de grafo de filtro. Chamando o [**método IFilterGraph::EnumFilters,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) o PID pode enumerar os filtros no grafo e distribuir chamadas de método para esses filtros. Dessa forma, um PID pode servir como um único ponto de controle para o aplicativo chamar métodos em filtros.

Quando o gerenciador de grafo de filtro agrega um PID, ele consulta o PID para a interface [**IDistributorNotify.**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) Se o PID for compatível com essa interface, o gerenciador de grafo de filtro o usará para notificar o PID sobre as alterações no grafo:

-   Quando o grafo de filtro alterna entre estados de run, paused e stopped, ele chama [**IDistributorNotify::Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause ou**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause) [**IDistributorNotify::Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Quando um relógio de referência é definido, o gerenciador de grafo de filtro chama [**IDistributorNotify::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Quando os filtros são adicionados ou removidos ou as conexões de pino são alteradas, o gerenciador de grafo de filtro chama [**IDistributorNotify::NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Para implementar um PID personalizado, crie um objeto COM que dá suporte à agregação. Ele deve dar suporte a uma interface que o gerenciador de grafo de filtro ainda não dá suporte. Opcionalmente, ele pode dar suporte à interface **IDistributorNotify.**

Se o PID obtiver ponteiros de interface do gerenciador de grafo de filtro, ele deverá liberá-los imediatamente. Caso contrário, ele poderá criar uma contagem de referência circular, o que pode impedir que o gerenciador de grafo de filtro seja destruído. Manter uma contagem de referência no gerenciador de grafo de filtro é desnecessário em qualquer caso, porque o gerenciador de grafo de filtro controla o tempo de vida do PID.

Como um PID foi projetado especificamente para agregação pelo gerenciador de grafo de filtro, talvez você queira impor isso no método do construtor do PID. Verifique se o ponteiro **IUnknown** externo é **NULL** e, se for o caso, retorne o código de erro VFW \_ E NEED \_ \_ OWNER. (Consulte [Códigos de erro e êxito](error-and-success-codes.md).) Além disso, para impedir que outros objetos agreguem o PID, você pode consultar o ponteiro **IUnknown** externo para a interface [**IGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) Retornar um código de erro se o objeto não expor **IGraphBuilder**.

 

 



