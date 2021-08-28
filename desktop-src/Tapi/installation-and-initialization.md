---
description: A instalação de um novo provedor de serviços é altamente específica do dispositivo e do sistema operacional, portanto, os detalhes estão fora do escopo desse SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Instalação e inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15dc5d9d93ce33ac13a04aec3abd7d49fec3ed2ece3cce691d47c0d617bacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003534"
---
# <a name="installation-and-initialization"></a>Instalação e inicialização

A instalação de um novo provedor de serviços é altamente específica do dispositivo e do sistema operacional, portanto, os detalhes estão fora do escopo desse SDK. Em termos gerais, o objetivo da instalação é a configuração do provedor de serviços para o ambiente de comunicação atual. Isso geralmente envolve entradas do Registro e a configuração de dependências de serviço.

A inicialização de um provedor de serviços de telefonia começa com a negociação de versão. Confira [Versão do TSPI para](tspi-versioning.md) ver uma discussão sobre a negociação de versão e a versão atual.

EM seguida, a TAPI chama o provedor [**TSPIInit, \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)que passa ao provedor um ponteiro para uma função de retorno de chamada usada para relatar o progresso de funções assíncronas. O TSP retorna uma contagem de dispositivos de linha e telefone associados ao identificador de dispositivo atual.

Normalmente, a próxima etapa será o inventário de recursos, realizado pela TAPI invocando a linha [**TSPIGetDevCaps \_**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) e a linha [**TSPIGetAddressCaps. \_**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps) Espera-se que o provedor de serviços preencha os elementos das estruturas de dados envolvidas que pertencem aos recursos de dispositivo e sessão aos que ele dá suporte.

A TAPI coleta informações de vários aplicativos referentes aos requisitos de notificação de eventos e instrui o TSP usando [**tSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) para indicar quais tipos de mídia detectar para uma linha e linha [**TSPISetStatusMessages \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) para indicar quais eventos de linha e endereço devem ser relatados.

 

 
