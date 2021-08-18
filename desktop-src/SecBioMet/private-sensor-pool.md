---
title: Pool de Sensor Privado
description: Uma coleção de unidades biométricas reservadas para uso exclusivo por um aplicativo cliente. Os pools privados suportam métodos de autenticação proprietários e permitem que um aplicativo cliente acesse uma unidade biométrica usando comandos de controle especificados pelo fornecedor.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306f4e0d4e28cfb29dda694e835348721113a5c23ec51054169537282ae2c365
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480436"
---
# <a name="private-sensor-pool"></a>Pool de Sensor Privado

Um pool de sensor privado é uma coleção de unidades biométricas reservadas para uso exclusivo por um aplicativo cliente. Os pools privados suportam métodos de autenticação proprietários e permitem que um aplicativo cliente acesse uma unidade biométrica usando comandos de controle especificados pelo fornecedor. Unidades biométricas em um pool de sensor privado:

-   Estão disponíveis somente para o aplicativo cliente que criou o pool.
-   Envie avisos de evento gerados pela conclusão de operações biométricas diretamente para o aplicativo sem considerar o foco da janela atual.
-   Use GUIDs para identificar modelos biométricos.
-   Compartilhar um banco de dados de modelo único e selecionado pelo aplicativo.

Os pools de sensor privados devem ser usados se o aplicativo cliente:

-   Gerencia uma coleção de unidades biométricas dedicadas que usam um banco de dados de modelo específico do aplicativo. Por exemplo, considere um aplicativo de participação de funcionários em que os funcionários sinalizam sua chegada no trabalho com o dedo em um leitor de impressão digital. Os funcionários não têm Windows contas no computador que executa o aplicativo. Em vez disso, suas impressões digitais são identificadas por GUIDs gerenciados pelo aplicativo de participação.
-   Coleta exemplos biométricos em vez de simplesmente mapeia amostras para SIDs.
-   Coloca o hardware de unidade biométrica no modo de manutenção para atualizar o firmware.
-   Envia comandos de controle definidos pelo fornecedor para o hardware ou software de unidade biométrica.
-   Tenta configurar uma unidade biométrica com armazenamento de integração para operar no modo avançado, mas a unidade não pode executar as operações de hash necessárias.
-   É executado de uma Área de Trabalho Remota cliente.

> [!Note]  
> Os aplicativos podem criar pools de sensor privados apenas para biometria por impressão digital. Se um aplicativo tentar criar um para qualquer outra coisa (por exemplo, Face), a solicitação falhará.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um pool de sensor privado](creating-a-private-sensor-pool.md)
</dt> <dt>

[Sensor Pools](sensor-pools.md)
</dt> <dt>

[Pool de Sensor do Sistema](system-sensor-pool.md)
</dt> </dl>

 

 




