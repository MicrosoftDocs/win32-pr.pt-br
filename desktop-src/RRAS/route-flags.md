---
title: Sinalizadores de rota
description: Sinalizadores de rota
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Rota
- Sinalizadores de rota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1476742f1204eb14dd2bb96b289825d179a58e5bec01ff0aee18bcfbdb13a9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081236"
---
# <a name="route-flags"></a>Sinalizadores de rota

## <a name="state-of-the-route-constants"></a>Estado das constantes de rota



| Constante                    | Valor | Descrição             |
|-----------------------------|-------|-------------------------|
| ESTADO DE \_ ROTA RTM \_ \_ CRIADO  | 0     | A rota foi criada. |
| EXCLUSÃO DE \_ ESTADO \_ DE ROTA \_ RTM | 1     | A rota está sendo excluída. |
| ESTADO DE \_ ROTA RTM \_ \_ EXCLUÍDO  | 2     | A rota foi excluída. |



 

## <a name="route-update-flags"></a>Sinalizadores de atualização de rota



| Constante                  | Valor      | Descrição                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALTERAÇÃO DE \_ ROTA \_ RTM \_ PRIMEIRO | 0x01       | Indica que o gerenciador de tabelas de roteamento não deve verificar o membro **Desamando** da estrutura [**RTM ROUTE \_ \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) ao determinar quando duas rotas são iguais. |
| ALTERAÇÃO DE \_ ROTA \_ RTM \_ NOVA   | 0x02       | Retornado pelo gerenciador de tabela de roteamento para indicar que uma nova rota foi criada.                                                                                                                 |
| ALTERAÇÃO DE \_ ROTA RTM \_ \_ MELHOR  | 0x00010000 | Retornado pelo gerenciador de tabela de roteamento para indicar que a rota que foi adicionada ou atualizada era a melhor rota ou que, devido à alteração, uma nova rota se tornou a melhor rota.           |



 

## <a name="unicast-flags"></a>Sinalizadores Unicast



| Constante                  | Valor  | Descrição                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| SINALIZADORES \_ DE \_ ROTA RTM \_ LOCAIS  | 0x0010 | Indica que um destino está em uma rede diretamente acessível.            |
| SINALIZADORES \_ DE ROTA \_ RTM \_ REMOTOS | 0x0020 | Indica que o destino não está em uma rede diretamente acessível. |
| SINALIZADORES \_ DE \_ ROTA RTM POR MIM \_ MESMO | 0x0040 | Indica que o destino é um dos endereços do roteador.            |



 

## <a name="broadcast-and-multicast-flags"></a>Sinalizadores de difusão e multicast



| Constante                           | Valor  | Descrição                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCAST \_ DE \_ SINALIZADORES DE ROTA \_ RTM           | 0x0100 | Indica que essa rota é uma rota para um endereço multicast.                                                                                                                                               |
| RTM \_ ROUTE \_ FLAGS \_ LOCAL \_ MCAST    | 0x0200 | Indica que essa rota é uma rota para um endereço multicast local.                                                                                                                                         |
| BC LIMITADO \_ DE SINALIZADORES \_ DE ROTA \_ RTM \_     | 0x0400 | Indica que essa rota é um endereço de difusão limitado. Os pacotes para esse destino não devem ser encaminhados.                                                                                             |
| RTM \_ ROUTE \_ SINALIZA \_ ZEROS \_ NETBC    | 0x1000 | Indica que o destino corresponde ao endereço de difusão de todos os zeros de uma interface. Se o encaminhamento de difusão estiver habilitado, os pacotes deverão ser recebidos e reabilitar todas as interfaces apropriadas.               |
| RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | 0x2000 | Indica que o destino corresponde ao endereço de difusão de sub-rede all-zeros de uma interface. Se o encaminhamento de difusão de sub-rede estiver habilitado, os pacotes deverão ser recebidos e reabilitar todas as interfaces apropriadas. |
| RTM \_ ROUTE \_ FLAGS \_ ONES \_ NETBC     | 0x4000 | Indica que o destino corresponde ao endereço de difusão de todos os da interface. Se o encaminhamento de difusão estiver habilitado, os pacotes deverão ser recebidos e reabilitar todas as interfaces apropriadas.                |
| SUB-REDE DE \_ SINALIZADORES \_ DE ROTA \_ \_ RTM  | 0x8000 | Indica que o destino corresponde ao endereço de difusão de sub-rede all-ones de uma interface. Se o encaminhamento de difusão de sub-rede estiver habilitado, os pacotes deverão ser recebidos e reabilitar todas as interfaces apropriadas.  |



 

## <a name="grouping-of-flags"></a>Agrupamento de sinalizadores



| Agrupar                            | Membros                                                                                                                                                                  | Descrição                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| ENCAMINHAMENTO DE \_ SINALIZADORES \_ DE ROTA RTM \_    | SINALIZADORES DE ROTA RTM, SINALIZADORES DE ROTA RTM BLACKHOLE, DESCARTE DE SINALIZADORES DE ROTA \_ \_ \_ \_ \_ \_ RTM, SINALIZADORES DE ROTA \_ \_ \_ RTM \_ \_ \_ INATIVOS                                                        | Especifica os sinalizadores de encaminhamento.                          |
| A ROTA RTM \_ \_ SINALIZA QUALQUER \_ \_ UNICAST  | SINALIZADORES \_ DE ROTA \_ RTM \_ LOCAIS, SINALIZADORES DE ROTA RTM \_ \_ \_ REMOTOS, SINALIZADORES DE ROTA RTM \_ POR MIM \_ \_ MESMO                                                                                           | Especifica quaisquer sinalizadores unicast.                             |
| A ROTA \_ RTM \_ SINALIZA QUALQUER \_ \_ MCAST    | RTM \_ ROUTE \_ FLAGS \_ MCAST, RTM \_ ROUTE \_ FLAGS \_ LOCAL \_ MCAST                                                                                                                | Especifica quaisquer sinalizadores unicast.                             |
| \_BCAST DE SUB-REDE DE SINALIZADORES DE \_ \_ ROTA \_ RTM | RTM \_ SINALIZA \_ UMA SUB-REDE \_ \_ \_ BC, RTM \_ ROUTE SINALIZA \_ \_ ZEROS \_ SUBNETBC                                                                                                  | Especifica todos os sinalizadores de difusão de sub-rede.                    |
| RTM \_ ROUTE \_ FLAGS \_ NET \_ BCAST    | SINALIZADORES \_ DE \_ ROTA RTM \_ \_ NETBC, RTM \_ ROUTE SINALIZA \_ \_ ZEROS \_ NETBC                                                                                                          | Especifica todos os sinalizadores de difusão em toda a rede.                  |
| RTM \_ ROUTE SINALIZA QUALQUER \_ \_ \_ BCAST    | SINALIZADORES DE ROTA RTM BC LIMITADOS, SINALIZADORES DE ROTA \_ \_ \_ \_ RTM NETBC, SINALIZADORES DE ROTA \_ \_ \_ \_ RTM \_ UNS \_ SUB-REDE \_ \_ \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | Especifica qualquer uma das sub-redes ou sinalizadores de difusão em toda a rede. |



 

 

 




