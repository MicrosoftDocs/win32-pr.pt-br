---
description: O instalador executará a sequência do assistente de instalação de exemplo somente se o nível completo da interface do usuário for usado para instalar o aplicativo.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Adicionar um evento de controle ao final da instalação para executar a inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cf2a32a30187ea263bd2e3530e6eaae7d236e111826cbcab2461746d9c8e48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078216"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Adicionar um evento de controle ao final da instalação para executar a inicialização

O instalador executará a sequência do assistente de instalação de exemplo somente se o nível [*completo da interface do usuário*](f-gly.md) for usado para instalar o aplicativo. A última caixa de diálogo da sequência de diálogo de exemplo é uma caixa de [diálogo de saída](exit-dialog.md) chamada ExitDialog. Quando um usuário interage com o botão OK em ExitDialog, isso primeiro publica um [ControlEvent, EndDialog](enddialog-controlevent.md) que retorna o controle ao instalador. Em seguida, o controle publica um [ControlEvent, DoAction](doaction-controlevent.md) que executa a ação personalizada de inicialização. Cada evento de controle requer um registro na [tabela ControlEvent,](controlevent-table.md). Consulte [visão geral do ControlEvent,](controlevent-overview.md).

[Tabela ControlEvent,](controlevent-table.md)



| caixa de diálogo     | controle\_ | Evento     | Argumento | Condição                     | Ordenando |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | OK        | EndDialog | Retorno   | 1                             | 1        |
| ExitDialog | OK        | DoAction  | Inicializar   | NÃO instalado e $Tutorial = 3 | 2        |



 

A condição no controle DoAction garante que a ação personalizada só seja executada durante a primeira instalação do aplicativo e que esteja sendo instalada localmente. A frase $Tutorial = 3 significa que o estado de ação do componente tutorial está definido como local. Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

Isso conclui o exemplo.

 

 



