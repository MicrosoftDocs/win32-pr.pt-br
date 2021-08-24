---
title: Visão geral do DNS
description: O DNS é um serviço padrão do setor usado para localizar computadores em uma rede baseada em PROTOCOLO IP.
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a47874606491c1baf5c52ca7934d7e0c3156a6ab99f9726e6c000d9eb3cb65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967466"
---
# <a name="dns-overview"></a>Visão geral do DNS

O DNS é um serviço padrão do setor usado para localizar computadores em uma rede baseada em PROTOCOLO IP. Redes IP, como a Internet e Windows 2000, dependem de endereços baseados em número, como 207.46.131.137 para transportar informações em toda a rede. Os usuários de rede dependem de nomes baseados em caracteres, como `www.microsoft.com` . Portanto, é necessário converter caracteres ou endereços amigáveis ( ) nos endereços baseados em número `www.microsoft.com` (207.46.131.137) que a rede possa reconhecer. DNS é o serviço de escolha no Windows 2000 para localizar recursos e traduzi-los em seus endereços IP correspondentes.

O DNS usa um banco de dados especializado de registros de recursos, normalmente chamado de RRs, para responder a consultas de resolução de nomes do cliente. Antes do DNS, a resolução de nomes na Internet era alcançada com o arquivo [*de hosts*](h-gly.md), que são arquivos criados manualmente que associaram nomes de host a endereços IP.

Quando um novo cliente foi adicionado à rede, um administrador precisava atualizar manualmente o arquivo de hosts e, em seguida, copiar (replicar) esse arquivo para todos os outros computadores na rede para que o novo host pudesse ser alcançado por todos. À medida que a Internet cresce, essa forma de resolução de nomes era claramente insuficiente; era muito intensivo de gerenciamento e não [*escalava*](s-gly.md). O arquivo de hosts acabou de ficar maior e, como ele usou um espaço de nome simples [*(consulte*](f-gly.md) também Name [Space),](name-space.md)ele não pôde ser particionado e teve que ser distribuído em sua totalidade. A solução era DNS.

-   O DNS substituiu o espaço de nome simples do arquivo de hosts por um [*espaço de nome hierárquico*](h-gly.md). Com um espaço de nome hierárquico, informações sobre nomes de host e endereços IP podem ser particionadas e distribuídas; portanto, a escalabilidade é alcançada. Por exemplo, no domínio fictício widgets.products.microsoft.com, a responsabilidade pela resolução de nomes pode ser particionada para que vários servidores possam lidar com a resolução de nomes para diferentes partes do espaço de nome:
    -   Um servidor pode ser responsável por resolver a primeira parte (microsoft.com) e, em seguida, pode encaminhar a solicitação de resolução de nomes para o próximo Servidor DNS na hierarquia.
    -   O próximo servidor DNS pode ser responsável por resolver a próxima parte do espaço de nome (produtos).
    -   Por fim, a solicitação pode ser encaminhada para um terceiro servidor DNS responsável por resolver a última parte do nome (widgets).

Os Servidores DNS em cada parte do espaço de nome hierárquico precisam manter um banco de dados de registros de recursos para hosts, mas apenas em sua parte da hierarquia. Portanto, o servidor (ou servidores) na parte de produtos do widgets.products.microsoft.com mantém RRs apenas para a parte de produtos do espaço de nome hierárquico , não para a parte microsoft.com ou a parte widgets do espaço de nome.

 

 




