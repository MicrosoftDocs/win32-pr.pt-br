---
title: Detalhes da implementação do DVC
description: Esta seção contém informações sobre como gravar um módulo de cliente de canal virtual dinâmico (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769388"
---
# <a name="dvc-implementation-details"></a>Detalhes da implementação do DVC

Esta seção contém informações sobre como gravar um módulo de cliente de canal virtual dinâmico (DVC).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Escrevendo um módulo de DVC de cliente](writing-a-client-dvc-component.md)
</dt> <dd>

Para gravar um módulo de cliente de canal virtual dinâmico (DVC), você deve primeiro implementar e registrar um plug-in de cliente Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[Registro de plug-in do DVC](dvc-plug-in-registration.md)
</dt> <dd>

Descreve a sintaxe para a entrada de plug-in de canal virtual dinâmico (DVC) para o cliente de Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[Iniciando um ouvinte DVC](starting-a-dvc-listener.md)
</dt> <dd>

Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) em execução no cliente e servidor do Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.

</dd> <dt>

[Aceitando uma conexão](accepting-a-connection.md)
</dt> <dd>

Em algum momento, o cliente do DVC (canal virtual dinâmico) solicitará uma conexão com o ouvinte DVC.

</dd> <dt>

[Gravando dados usando um canal DVC](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente.

</dd> <dt>

[Testando e Depurando](testing-and-debugging.md)
</dt> <dd>

Há um ouvinte de "eco" que é implementado pelo cliente de Conexão de Área de Trabalho Remota (RDC), que está sempre presente e escutando conexões de entrada.

</dd> <dt>

[Exemplo de plug-in de cliente DVC](dvc-client-plug-in-example.md)
</dt> <dd>

Exemplo de código C++ que mostra como criar um plug-in de Conexão de Área de Trabalho Remota (RDC) cliente Dynamic virtual Channel (DVC).

</dd> <dt>

[Exemplo de módulo de servidor DVC](dvc-server-component-example.md)
</dt> <dd>

Exemplo de código C++ que mostra como criar o módulo DVC (canal virtual dinâmico) do lado do servidor.

</dd> </dl>

 

 




