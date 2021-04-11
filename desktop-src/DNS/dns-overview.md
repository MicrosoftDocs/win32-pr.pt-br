---
title: Visão geral do DNS
description: O DNS é um serviço padrão do setor usado para localizar computadores em uma rede baseada em IP (Internet Protocol).
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470807a5775b022834a3ca2f0ee3f91db8bdd5de
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172901"
---
# <a name="dns-overview"></a>Visão geral do DNS

O DNS é um serviço padrão do setor usado para localizar computadores em uma rede baseada em IP (Internet Protocol). Redes IP, como as redes Internet e Windows 2000, dependem de endereços baseados em número, como 207.46.131.137 para ferry informações em toda a rede. Os usuários de rede dependem de nomes baseados em caracteres, como `www.microsoft.com` . Portanto, é necessário converter caracteres ou endereços amigáveis ( `www.microsoft.com` ) em endereços com base em números (207.46.131.137) que a rede pode reconhecer. O DNS é o serviço de sua escolha no Windows 2000 para localizar recursos e convertê-los em seus endereços IP correspondentes.

O DNS usa um banco de dados especializado de registros de recursos, comumente conhecido como RRs, para responder a consultas de resolução de nomes de cliente. Antes do DNS, a resolução de nomes na Internet foi obtida com o [*arquivo de hosts*](h-gly.md), que são manualmente criados para os nomes de host associados aos endereços IP.

Quando um novo cliente foi adicionado à rede, um administrador precisava atualizar manualmente o arquivo de hosts e, em seguida, copiar (replicar) esse arquivo para todos os outros computadores na rede para que o novo host pudesse ser alcançado por todos. À medida que a Internet cresceu, essa forma de resolução de nomes era claramente insuficiente; Ele era muito intensivo de gerenciamento e não foi [*dimensionado*](s-gly.md). O arquivo de hosts acabou de ser maior, e como ele usou um [*espaço de nome simples*](f-gly.md) (consulte também o [espaço de nome](name-space.md)), ele não pôde ser particionado e teve que ser distribuído em sua totalidade. A solução era DNS.

-   O DNS substituiu o espaço de nome simples do arquivo de hosts por um [*espaço de nome hierárquico*](h-gly.md). Com um espaço de nome hierárquico, as informações sobre nomes de host e endereços IP podem ser particionadas e distribuídas; Portanto, a escalabilidade é alcançada. Por exemplo, no domínio fictício widgets.products.microsoft.com, a responsabilidade pela resolução de nomes pode ser particionada para que vários servidores possam lidar com a resolução de nomes para diferentes partes do espaço de nome:
    -   Um servidor pode ser responsável por resolver a primeira parte (microsoft.com) e, em seguida, pode encaminhar a solicitação de resolução de nomes para o próximo servidor DNS na hierarquia.
    -   O próximo servidor DNS pode ser responsável por resolver a próxima parte do espaço de nome (produtos).
    -   Por fim, a solicitação pode ser encaminhada para um terceiro servidor DNS responsável por resolver a última parte do nome (widgets).

Os servidores DNS em cada parte do espaço de nomes hierárquicos precisam manter um banco de dados de registros de recursos para hosts, mas apenas em sua parte da hierarquia. Portanto, o servidor (ou servidores) na parte produtos da widgets.products.microsoft.com mantém RRs somente para os produtos que fazem parte do espaço de nome hierárquico — não para a parte microsoft.com ou os widgets que fazem parte do espaço de nome.

 

 




