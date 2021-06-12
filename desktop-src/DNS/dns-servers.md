---
title: Servidores DNS
description: Saiba mais sobre servidores DNS. Um Servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011249"
---
# <a name="dns-servers"></a>Servidores DNS

Um *Servidor DNS* é um computador que conclui o processo de resolução de nomes no DNS. Os Servidores DNS [*contêm arquivos de zona*](z-gly.md) que permitem resolver nomes para endereços IP e endereços IP para nomes. Quando consultado, um servidor DNS responderá de uma das três maneiras:

-   O servidor retorna os dados solicitados de resolução de nome ou resolução de IP.
-   O servidor retorna um ponteiro para outro servidor DNS que pode fazer o serviço da solicitação.
-   O servidor indica que ele não tem os dados solicitados.

Os Servidores DNS podem, durante a preparação para retornar os dados de resolução solicitados, consultar outros Servidores DNS, mas além disso, os Servidores DNS não executam nenhuma outra operação.

Há três tipos principais de servidores DNS : servidores primários, servidores secundários e servidores de cache.

## <a name="primary-server"></a>Servidor Primário

O *servidor primário* é o servidor autoritativo para a zona. Todas as tarefas administrativas associadas à zona (como criar subdomasins dentro da zona ou outras tarefas administrativas semelhantes) devem ser executadas no servidor primário. Além disso, todas as alterações associadas à zona ou quaisquer modificações ou adições a RRs nos arquivos de zona devem ser feitas no servidor primário. Para qualquer zona, há um servidor primário, exceto quando você integra os serviços do Active Directory e o Servidor DNS da Microsoft.

## <a name="secondary-servers"></a>Servidores secundários

*Os servidores secundários* são servidores DNS de backup. Os servidores secundários recebem todos os arquivos de zona dos arquivos de zona do servidor primário em uma transferência de zona. Vários servidores secundários podem existir para qualquer zona determinada – tantos quantos necessários para fornecer balanceamento de [*carga,*](l-gly.md)tolerância a falhas [*e*](f-gly.md)redução de tráfego. Além disso, qualquer servidor DNS específico pode ser um servidor secundário para várias zonas.

Além dos Servidores DNS primários e secundários, funções adicionais do Servidor DNS podem ser usadas quando esses servidores são apropriados para uma infraestrutura DNS. Esses servidores adicionais são servidores e encaminhadores [*de cache.*](f-gly.md)

## <a name="caching-servers"></a>Servidores de cache

[*Servidores de cache*](c-gly.md), também conhecidos como servidores somente cache, executam como o nome sugere; eles fornecem apenas o serviço de consulta armazenado em cache para respostas DNS. Em vez de manter arquivos de zona como outros servidores secundários, o cache de servidores DNS executa consultas, armazena em cache as respostas e retorna os resultados para o cliente de consulta. A principal diferença entre servidores de cache e outros servidores secundários é que outros servidores secundários mantêm arquivos de zona (e fazem transferências de zona quando apropriado, gerando assim o tráfego de rede associado à transferência), os servidores de cache não.

 

 




