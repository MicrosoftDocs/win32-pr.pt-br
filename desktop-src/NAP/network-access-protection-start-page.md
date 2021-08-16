---
title: Proteção de Acesso à Rede
description: 'observação: a plataforma de proteção de acesso à rede não está disponível a partir do Windows 10 NAP (proteção de acesso à rede) é um conjunto de componentes do sistema operacional que fornecem uma plataforma para acesso protegido a redes privadas.'
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Proteção de Acesso à Rede
- Proteção de acesso à rede, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e5b5121566c3626ee7a9f2ba5d85efc1bf6cff17b412cd99874ae9b346780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939124"
---
# <a name="network-access-protection"></a>Proteção de Acesso à Rede

## <a name="purpose"></a>Finalidade

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A NAP (proteção de acesso à rede) é um conjunto de componentes do sistema operacional que fornece uma plataforma para acesso protegido a redes privadas. A plataforma NAP fornece uma maneira integrada de avaliar o estado de integridade do sistema de um cliente de rede que está tentando se conectar ou se comunicar em uma rede e restringir o acesso do cliente de rede até que os requisitos da política de integridade sejam atendidos.

A NAP é uma plataforma extensível que fornece uma infraestrutura e uma API definida para adicionar componentes que armazenam, relatam, validam e corrigem o estado de integridade do sistema de um computador. Por si só, a plataforma NAP não fornece componentes para acumular e avaliar os atributos do estado de integridade de um computador. Outros componentes, conhecidos como agentes de integridade do sistema (SHAs) e validadores da integridade do sistema (SHVs), fornecem validação de política de rede e conformidade de política de rede.

## <a name="where-applicable"></a>Quando aplicável

A NAP foi projetada para ser extensível. Ele pode interoperar com qualquer software de fornecedor que forneça SHAs e SHVs ou que reconheça seu conjunto de API publicado. A NAP ajuda a fornecer uma solução para os seguintes cenários comuns:

-   Verifique a integridade e o status dos laptops móveis.
-   Garanta a integridade dos computadores desktop.
-   Verifique a conformidade e a integridade dos computadores em escritórios remotos.
-   Determine a integridade dos laptops visitantes.
-   Verifique a conformidade e a integridade de computadores domésticos não gerenciados.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de NAP foi projetada para desenvolvedores de C/C++. Para os métodos de imposição de NAP, os programadores devem estar familiarizados com os protocolos de rede e as tecnologias, como o serviço de usuário dial-in de autenticação remota (RADIUS), protocolo DHCP, redes virtuais privadas (VPNs), o padrão IEEE 802.1 X para acesso com e sem fio e IPsec (Internet Protocol Security).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

a plataforma nap requer servidores de infraestrutura nap que executam o Windows Server 2008 ou posterior e clientes NAP executando o Windows XP com Service Pack 3 (SP3), Windows Vista ou sistemas operacionais posteriores. Para obter informações específicas sobre quais sistemas operacionais dão suporte a um determinado elemento de programação, consulte as seções de requisitos das APIs de NAP na documentação de referência de NAP.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                         | Descrição                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Sobre a NAP](about-nap.md)<br/>         | Informações gerais sobre a API NAP.<br/>                                     |
| [Usando NAP](using-nap.md)<br/>         | Exemplos de uso para a API NAP.<br/>                                            |
| [Referência de NAP](nap-reference.md)<br/> | Documentação para interfaces NAP, estruturas e outros elementos de código.<br/> |



 

 

 





