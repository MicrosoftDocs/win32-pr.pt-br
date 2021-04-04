---
title: Sinalizadores de rota
description: Sinalizadores de rota
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Rota
- Sinalizadores de rota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1711ef4ed621d55cc00302cca181676a3892c030
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916003"
---
# <a name="route-flags"></a>Sinalizadores de rota

## <a name="state-of-the-route-constants"></a>Estado das constantes de rota



| Constante                    | Valor | Descrição             |
|-----------------------------|-------|-------------------------|
| \_estado de rota RTM \_ \_ criado  | 0     | A rota foi criada. |
| \_exclusão do \_ estado da rota RTM \_ | 1     | A rota está sendo excluída. |
| \_estado da rota RTM \_ \_ excluído  | 2     | A rota foi excluída. |



 

## <a name="route-update-flags"></a>Sinalizadores de atualização de rota



| Constante                  | Valor      | Descrição                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_alteração de rota RTM \_ \_ primeiro | 0x01       | Indica que o Gerenciador de tabela de roteamento não deve verificar o membro **vizinho** da estrutura de [**\_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) ao determinar quando duas rotas são iguais. |
| \_ \_ nova alteração de rota RTM \_   | 0x02       | Retornado pelo Gerenciador de tabela de roteamento para indicar que uma nova rota foi criada.                                                                                                                 |
| \_ \_ melhor alteração de rota da RTM \_  | 0x00010000 | Retornado pelo Gerenciador de tabela de roteamento para indicar que a rota que foi adicionada ou atualizada foi a melhor rota, ou que devido à alteração, uma nova rota se tornou a melhor rota.           |



 

## <a name="unicast-flags"></a>Sinalizadores de unicast



| Constante                  | Valor  | Descrição                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| sinalizadores de rota do RTM \_ \_ \_ local  | 0x0010 | Indica que um destino está em uma rede acessível diretamente.            |
| \_sinalizadores de rota RTM \_ \_ remotos | 0x0020 | Indica que o destino não está em uma rede acessível diretamente. |
| \_sinalizadores de rota da RTM \_ \_ | 0x0040 | Indica que o destino é um dos endereços do roteador.            |



 

## <a name="broadcast-and-multicast-flags"></a>Sinalizadores de difusão e multicast



| Constante                           | Valor  | Descrição                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sinalizadores de rota do RTM \_ \_ \_ MCast           | 0x0100 | Indica que essa rota é uma rota para um endereço de multicast.                                                                                                                                               |
| \_ \_ mcast locais de sinalizadores de rota RTM \_ \_    | 0x0200 | Indica que essa rota é uma rota para um endereço de multicast local.                                                                                                                                         |
| \_ \_ BC limitada de sinalizadores de rota de \_ RTM \_     | 0x0400 | Indica que essa rota é um endereço de difusão limitado. Os pacotes para esse destino não devem ser encaminhados.                                                                                             |
| sinalizadores de rota da RTM \_ \_ \_ zeros \_ NETBC    | 0x1000 | Indica que o destino corresponde ao endereço de difusão de todos os zeros da interface. Se o encaminhamento de difusão estiver habilitado, os pacotes deverão ser recebidos e reenviados para todas as interfaces apropriadas.               |
| sinalizadores de rota da RTM \_ \_ \_ zeros \_ SUBNETBC | 0x2000 | Indica que o destino corresponde ao endereço de difusão de sub-rede de todos os zeros da interface. Se o encaminhamento de difusão de sub-rede estiver habilitado, os pacotes deverão ser recebidos e reenviados todas as interfaces apropriadas. |
| sinalizadores de rota do RTM \_ \_ \_ \_ NETBC     | 0x4000 | Indica que o destino corresponde ao endereço de difusão de todos os itens da interface. Se o encaminhamento de difusão estiver habilitado, os pacotes deverão ser recebidos e reenviados para todas as interfaces apropriadas.                |
| sinalizadores de rota do RTM \_ \_ \_ \_ SUBNETBC  | 0x8000 | Indica que o destino corresponde ao endereço de difusão de sub-rede de todos os itens da interface. Se o encaminhamento de difusão de sub-rede estiver habilitado, os pacotes deverão ser recebidos e reenviados todas as interfaces apropriadas.  |



 

## <a name="grouping-of-flags"></a>Agrupamento de sinalizadores



| Agrupar                            | Membros                                                                                                                                                                  | Descrição                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| \_ \_ encaminhamento de sinalizadores de rota RTM \_    | \_ \_ sinalizadores de rota RTM \_ MARTIAN, \_ sinalizadores de rota RTM \_ \_ BLACKHOLE \_ , \_ \_ descartar sinalizadores de rota RTM, \_ sinalizadores de rota RTM \_ \_ inativos                                                        | Especifica os sinalizadores de encaminhamento.                          |
| sinalizadores de rota da RTM \_ \_ \_ qualquer \_ unicast  | \_ \_ sinalizadores de rota RTM \_ local, \_ sinalizadores de rota RTM \_ \_ REMOTOs, sinalizadores de rota RTM para \_ \_ \_ mim mesmo                                                                                           | Especifica qualquer sinalizador de unicast.                             |
| sinalizadores de rota da RTM \_ \_ \_ qualquer \_ MCast    | \_ \_ sinalizadores de rota RTM \_ mcast, \_ sinalizadores de rota RTM \_ \_ \_ mcast locais                                                                                                                | Especifica qualquer sinalizador de unicast.                             |
| \_sinalizadores de rota RTM \_ \_ BCAST sub-rede \_ | os \_ sinalizadores de rota do RTM são a \_ \_ \_ sub-rede \_ BC, a \_ rota RTM \_ sinaliza \_ zeros \_ SUBNETBC                                                                                                  | Especifica qualquer sinalizador de difusão de sub-rede.                    |
| sinalizadores de rota do RTM \_ \_ \_ net \_ BCAST    | \_sinalizadores de rota da RTM \_ \_ \_ NETBC, \_ sinalizadores de rota da RTM \_ \_ zeros \_ NETBC                                                                                                          | Especifica qualquer sinalizador de difusão de toda a rede.                  |
| sinalizadores de rota da RTM \_ \_ \_ qualquer \_ BCAST    | sinalizadores de rota da RTM \_ \_ \_ Limited \_ BC, sinalizadores de rota do RTM \_ \_ \_ \_ NETBC, sinalizadores de rota da versão RTM \_ \_ \_ \_ \_ de BC, \_ sinalizadores de rota RTM \_ \_ zeros \_ NETBC, \_ sinalizadores de rota RTM \_ \_ zeros \_ SUBNETBC | Especifica qualquer um dos sinalizadores de difusão de sub-rede ou de toda a rede. |



 

 

 




