---
description: Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Provedores de serviços de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836952"
---
# <a name="telephony-service-providers"></a>Provedores de serviços de telefonia

## <a name="purpose"></a>Finalidade

Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas. Um aplicativo TAPI usa comandos padronizados, a TAPI passa informações para o provedor de serviços de telefonia e o TSP lida com os comandos específicos que devem ser trocados pelo dispositivo.

Um TSP deve estar em conformidade com a TSPI (interface do provedor de serviços de telefonia) para funcionar como um provedor de serviços no ambiente de telefonia da Microsoft. TSPI define as funções externas expostas por um provedor de serviços de telefonia fornecido com equipamentos de comunicação.

## <a name="developer-audience"></a>Público de desenvolvedores

Você pode gravar aplicativos habilitados para TAPI em várias linguagens, incluindo Java, Visual Basic e C/C++. A experiência de desenvolvimento anterior com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.

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

 

