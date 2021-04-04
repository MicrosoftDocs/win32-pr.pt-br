---
title: Arquitetura WFP
description: Esta seção fornece uma breve visão geral da arquitetura da plataforma de filtragem do Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162232"
---
# <a name="wfp-architecture"></a>Arquitetura WFP

A figura a seguir mostra a arquitetura básica da WFP (Windows Filtering Platform).

![arquitetura básica do diagrama da plataforma de filtragem do Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a>Mecanismo de filtro

O mecanismo de filtro contém um componente de modo de usuário e um componente de modo kernel, que juntos executam todas as operações de filtragem em dados de rede. O mecanismo de filtro contém várias camadas de filtragem que são mapeadas livremente para as camadas de pilha de rede do sistema operacional. As camadas do mecanismo de filtro são divididas em camadas de modo de usuário e camadas de modo kernel com base no componente do mecanismo de filtro que as possui.

O componente do modo de usuário executa a filtragem de RPC e IPsec. O mecanismo de filtro contém aproximadamente 10 camadas de filtragem de modo de usuário.

O componente do modo kernel executa a filtragem nas camadas de rede e de transporte da pilha de TC/IP. Esse componente também chama as funções de texto explicativo disponíveis durante o processo de [classificação](basic-operation.md) . O mecanismo de filtro contém aproximadamente 50 camadas de filtragem de modo kernel.

Consulte [**Filtrar identificadores de camada**](management-filtering-layer-identifiers-.md) para obter uma descrição de cada uma das camadas do mecanismo de filtro.

## <a name="base-filtering-engine"></a>Mecanismo de Filtragem Base

O BFE (mecanismo de filtragem base) é um serviço de modo de usuário (bfe.dll em execução em um processo de svchost.exe) que coordena os componentes da WFP. As tarefas principais executadas pelo BFE são adicionar e remover filtros do sistema, armazenar a configuração de filtro e impor a segurança de configuração de WFP. Os aplicativos se comunicam com o BFE por meio das [funções de gerenciamento de WFP](fwp-mgmt-functions.md).

## <a name="callout-drivers"></a>Drivers de texto explicativo

Os drivers de texto explicativo fornecem funcionalidade de filtragem adicional adicionando funções de texto explicativo personalizadas ao mecanismo de filtro em uma ou mais das camadas de filtragem do modo kernel. Os textos explicativos dão suporte a inspeção e pacote profundos, bem como à modificação do fluxo. Depois que um driver de texto explicativo tiver adicionado suas funções de texto explicativo ao mecanismo de filtro, os filtros que especificam uma função de texto explicativo de um determinado driver poderão ser adicionados ao processo de filtragem. Esses filtros podem ser adicionados por um aplicativo de gerenciamento de modo de usuário ou pelo próprio driver de texto explicativo. A interface do modo kernel, fornecida no kit de desenvolvimento do Windows, só deve ser usada quando necessário e não como um substituto para a API do modo de usuário.

> [!Note]  
> Para obter mais informações sobre drivers de texto explicativo, consulte a seção Windows Filtering Platform do [Kit de desenvolvimento do Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

A plataforma de filtragem do Windows inclui uma série de funções de texto explicativo internas que podem ser usadas para comunicação de dados segura IPsec, configurações de filtragem com estado e filtragem de modo furtivo. Consulte [**identificadores de texto explicativo interno**](built-in-callout-identifiers.md) para obter uma lista completa de funções de texto explicativo internas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto](object-model.md)
</dt> <dt>

[Operação WFP](basic-operation.md)
</dt> <dt>

[Drivers de texto explicativo da plataforma de filtragem do Windows – guia de design](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Drivers de texto explicativo da plataforma de filtragem do Windows-referência](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 