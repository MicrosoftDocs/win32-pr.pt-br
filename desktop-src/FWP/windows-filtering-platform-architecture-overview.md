---
title: Arquitetura do WFP
description: Esta seção fornece uma breve visão geral da arquitetura Windows De filtragem de dados.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41989a11ff5412b3185f6987f9588f0309c3fde3ca386c71e4613ab6bc8237f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766596"
---
# <a name="wfp-architecture"></a>Arquitetura do WFP

A figura a seguir mostra a arquitetura básica do WFP (Windows Filtering Platform).

![arquitetura básica do diagrama da plataforma de filtragem de janelas](images/wfp-architecture.png)

## <a name="filter-engine"></a>Mecanismo de Filtro

O mecanismo de filtro contém um componente de modo de usuário e um componente de modo kernel, que juntos executam todas as operações de filtragem em dados de rede. O mecanismo de filtro contém várias camadas de filtragem que mapeiam livremente para as camadas de pilha de rede do sistema operacional. As camadas do mecanismo de filtro são divididas em camadas de modo de usuário e camadas de modo kernel com base no componente do mecanismo de filtro que as possui.

O componente de modo de usuário executa filtragem RPC e IPsec. O mecanismo de filtro contém aproximadamente 10 camadas de filtragem de modo de usuário.

O componente de modo kernel executa a filtragem nas camadas de rede e transporte da pilha TC/IP. Esse componente também chama as funções de chamada disponíveis durante o processo [de classificação.](basic-operation.md) O mecanismo de filtro contém aproximadamente 50 camadas de filtragem de modo kernel.

Consulte [**Filtrando identificadores de camada para**](management-filtering-layer-identifiers-.md) ver uma descrição de cada uma das camadas do mecanismo de filtro.

## <a name="base-filtering-engine"></a>Mecanismo de Filtragem Base

O BFE (Mecanismo de Filtragem Base) é um serviço de modo de usuário (bfe.dll em execução em um processo de svchost.exe) que coordena os componentes do WFP. As principais tarefas executadas pelo BFE são adicionar e remover filtros do sistema, armazenar a configuração de filtro e impor a segurança de configuração do WFP. Os aplicativos se comunicam com o BFE por meio [das funções de gerenciamento do WFP](fwp-mgmt-functions.md).

## <a name="callout-drivers"></a>Drivers de chamada

Os drivers de chamada fornecem funcionalidades de filtragem adicionais adicionando funções de chamada personalizadas ao mecanismo de filtro em uma ou mais camadas de filtragem de modo kernel. Os textos explicadores de chamada suportam inspeção profunda e pacote, bem como modificação de fluxo. Depois que um driver de chamada tiver adicionado suas funções de saída ao mecanismo de filtro, os filtros que especificam uma determinada função de chamada do driver poderão ser adicionados ao processo de filtragem. Esses filtros podem ser adicionados por um aplicativo de gerenciamento de modo de usuário ou pelo próprio driver de chamada. A interface de modo kernel, entregue no Windows Development Kit, só deve ser usada quando necessário e não como um substituto para a API de modo de usuário.

> [!Note]  
> Para obter mais informações sobre drivers de chamada, consulte a seção Windows filtering platform do [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

A Windows de Filtragem inclui várias funções de chamada internas que podem ser usadas para comunicação de dados seguros IPsec, configurações de filtragem com estado e filtragem de modo furtivo. Consulte [**Identificadores de chamada integrados**](built-in-callout-identifiers.md) para ver uma lista completa de funções de explicação de chamada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto](object-model.md)
</dt> <dt>

[Operação WFP](basic-operation.md)
</dt> <dt>

[Windows Filtrando drivers de chamada da plataforma – Guia de design](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Windows Filtrando drivers de chamada da plataforma – Referência](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 