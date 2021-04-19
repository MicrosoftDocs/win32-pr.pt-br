---
description: A instalação de um novo provedor de serviços é altamente específica do dispositivo e do sistema operacional, portanto, os detalhes estão fora do escopo deste SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Instalação e inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796328"
---
# <a name="installation-and-initialization"></a>Instalação e inicialização

A instalação de um novo provedor de serviços é altamente específica do dispositivo e do sistema operacional, portanto, os detalhes estão fora do escopo deste SDK. Em geral, o objetivo da instalação é a configuração do provedor de serviços para o ambiente de comunicação atual. Isso geralmente envolve entradas de registro e a configuração de dependências de serviço.

A inicialização de um provedor de serviços de telefonia começa com a negociação de versão. Consulte [controle de versão do TSPI](tspi-versioning.md) para uma discussão sobre negociação de versão e versão atual.

Em seguida, a TAPI chama [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), que passa o provedor de um ponteiro para uma função de retorno de chamada usada para relatar o progresso das funções assíncronas. O TSP retorna uma contagem de dispositivos de linha e telefone associados ao identificador de dispositivo atual.

Normalmente, a próxima etapa será o inventário de recursos, conduzido pela TAPI invocando [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) e [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). O provedor de serviços deve preencher esses elementos das estruturas de dados envolvidas que pertencem aos recursos de dispositivo e de sessão que ele suporta.

A TAPI coleta informações de vários aplicativos relacionados aos requisitos de notificação de eventos e instrui o TSP usando [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) para indicar quais tipos de mídia serão detectados para uma linha e [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) para indicar quais eventos de linha e endereço devem ser relatados.

 

 
