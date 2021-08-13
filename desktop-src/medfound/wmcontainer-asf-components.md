---
description: Os objetos WMContainer fornecem um controle de baixo nível sobre a análise e a gravação de um arquivo ASF (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componentes ASF WMContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4d39edd9241a856d5ef854d91bc1198cb090ddf653960b19905407c28279a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736734"
---
# <a name="wmcontainer-asf-components"></a>Componentes ASF WMContainer

Os objetos WMContainer fornecem um controle de baixo nível sobre a análise e a gravação de um arquivo ASF (Advanced Systems Format).

Os [componentes ASF da camada de pipeline](pipeline-layer-asf-components.md) usam os objetos WMContainer internamente. A maioria dos aplicativos deve usar os componentes de pipeline, em vez de usar objetos WMContainer. Use WMContainer somente se você precisar de controle de baixo nível sobre a análise e a gravação de um arquivo ASF.

A camada WMContainer inclui os seguintes objetos:

-   [Perfil ASF](asf-profile.md)
-   [Objeto ASF ContentInfo](asf-contentinfo-object.md)
-   [Divisor de ASF](asf-splitter.md)
-   [Multiplexador ASF](asf-multiplexer.md)
-   [Indexador ASF](asf-index-object.md)

Os tópicos a seguir contêm instruções passo a passo sobre como usar o WMContainer para ler ou gravar arquivos ASF.

-   [Tutorial: lendo um arquivo ASF usando objetos WMContainer](tutorial--reading-an-asf-file.md)
-   [Tutorial: copiando Fluxos ASF usando objetos WMContainer](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Tutorial: gravando um arquivo WMA usando objetos WMContainer](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Sobre o contêiner do WM

Os objetos WMContainer interagem diretamente com objetos de arquivo ASF. O diagrama a seguir mostra a estrutura do arquivo ASF e os objetos WMContainer correspondentes.

![diagrama mostrando a estrutura do arquivo ASF e os objetos do Media Foundation correspondentes](images/asf-components01.png)

Exceto para o divisor e o multiplexador, cada um desses objetos dá suporte à análise (leitura) e à gravação de arquivos ASF. O divisor é usado apenas para ler arquivos ASF. O multiplexador é usado apenas para criar novos arquivos ASF.

Todas as operações executadas por objetos WMContainer são síncronas, o que significa que elas bloqueiam o thread de chamada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



