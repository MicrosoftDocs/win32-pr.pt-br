---
description: Distribuidores de plug-in
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Distribuidores de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7817e5e31b29444cc596b0be583be2198adc018
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105800051"
---
# <a name="plug-in-distributors"></a>Distribuidores de plug-in

Os distribuidores de plug-in (PIDs) são uma maneira de estender a funcionalidade do Gerenciador de gráfico de filtro. Um distribuidor de plug-in é um objeto COM que o Gerenciador do grafo de filtro agrega em tempo de execução. Os aplicativos obtêm acesso ao PID por meio do Gerenciador do grafo de filtro.

Quando o Gerenciador de grafo de filtro é consultado em busca de uma interface para a qual não oferece suporte, ele pesquisa o registro em busca de uma chave com o seguinte formato:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` é uma cadeia de caracteres que contém o identificador de interface. Se a entrada do registro existir, o valor da entrada definirá o identificador de classe (CLSID) de um PID que dá suporte à interface. O Gerenciador de gráfico de filtro agrega a PID e retorna um ponteiro de interface, agindo assim como o **IUnknown** externo para o PID. Quando o aplicativo chama métodos na interface, ele está, na verdade, chamando-os na PID. No entanto, a existência do PID é transparente para o aplicativo.

O termo *distribuidor* origina-se do fato de que um PID pode consultar seu ponteiro de **IUnknown** externo para interfaces no Gerenciador do grafo de filtro. Chamando o método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , o PID pode enumerar os filtros no grafo e distribuir chamadas de método para esses filtros. Dessa forma, um PID pode servir como um único ponto de controle para que o aplicativo chame métodos em filtros.

Quando o Gerenciador de gráfico de filtro agrega um PID, ele consulta o PID para a interface [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) . Se o PID der suporte a essa interface, o Gerenciador de gráfico de filtro o usará para notificar o PID sobre as alterações no grafo:

-   Quando o gráfico de filtro alterna entre os Estados de execução, pausa e parada, ele chama [**IDistributorNotify:: Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)ou [**IDistributorNotify:: Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Quando um relógio de referência é definido, o Gerenciador do grafo de filtro chama [**IDistributorNotify:: Setsyncname**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Quando os filtros são adicionados ou removidos, ou as conexões de fixação são alteradas, o Gerenciador de grafo de filtro chama [**IDistributorNotify:: NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Para implementar um PID personalizado, crie um objeto COM que ofereça suporte à agregação. Ele deve dar suporte a uma interface que o Gerenciador de gráfico de filtro ainda não suporta. Opcionalmente, ele pode dar suporte à interface **IDistributorNotify** .

Se o PID obtiver qualquer ponteiro de interface do Gerenciador de gráfico de filtro, ele deverá liberá-los imediatamente. Caso contrário, ele pode criar uma contagem de referência circular, o que pode impedir que o Gerenciador do grafo de filtro seja destruído. Manter uma contagem de referência no Gerenciador do grafo de filtro é desnecessário em qualquer caso, porque o Gerenciador do grafo de filtro controla o tempo de vida do PID.

Como um PID é projetado especificamente para agregação pelo Gerenciador do grafo de filtro, talvez você queira impor isso no método de construtor da PID. Verifique se o ponteiro de **IUnknown** externo é **nulo** e, nesse caso, retorne o código de erro VFW \_ E precisa de \_ \_ proprietário. (Consulte [códigos de erro e êxito](error-and-success-codes.md).) Além disso, para impedir que outros objetos agregam o PID, você pode consultar o ponteiro de **IUnknown** externo para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Retorna um código de erro se o objeto não expõe **IGraphBuilder**.

 

 



