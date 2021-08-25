---
description: Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Provedores de serviços de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1e7ff98bfbc898a419e385be07ebdae56d2067061d2ac7951b8c0aff42dcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872866"
---
# <a name="telephony-service-providers"></a>Provedores de serviços de telefonia

## <a name="purpose"></a>Finalidade

Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas. Um aplicativo TAPI usa comandos padronizados, a TAPI passa informações para o provedor de serviços de telefonia e o TSP lida com os comandos específicos que devem ser trocados pelo dispositivo.

Um TSP deve estar em conformidade com a TSPI (interface do provedor de serviços de telefonia) para funcionar como um provedor de serviços no ambiente de telefonia da Microsoft. TSPI define as funções externas expostas por um provedor de serviços de telefonia fornecido com equipamentos de comunicação.

## <a name="developer-audience"></a>Público de desenvolvedores

você pode gravar aplicativos habilitados para TAPI em várias linguagens, incluindo Java, Visual Basic e C/C++. A experiência de desenvolvimento anterior com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O TSPI permite o desenvolvimento de TSPs para todas as versões do Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                | Descrição                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Visão geral](about-the-telephony-service-provider-tsp-.md)<br/> | Informações gerais sobre a arquitetura e os componentes do TSPI.<br/> |
| [Referência](tspi-reference.md)<br/>                           | Documentação para as interfaces TSPI.<br/>                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de telefonia da Microsoft](./microsoft-telephony-overview.md)
</dt> <dt>

[Provedores de serviços de mídia](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2,2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3,1](./tapi-3-1-start-page.md)
</dt> </dl>

 

