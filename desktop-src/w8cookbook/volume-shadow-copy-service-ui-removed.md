---
title: Interface do usuário de versões anteriores removida para volumes locais
description: Interface do usuário de versões anteriores removida para volumes locais
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104454407"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>Interface do usuário de versões anteriores removida para volumes locais

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

As versões anteriores do Windows permitiam que os usuários restaurassem versões anteriores de arquivos individuais de "cópias de sombra" de volumes locais. Essas cópias de sombra são criadas pelo recurso "versões anteriores" por meio do VSS (serviço de cópias de sombra de volume). No Windows 7, os usuários podem configurar e agendar cópias de sombra na interface do usuário de proteção do sistema disponível por meio de propriedades do sistema.

No entanto, as versões anteriores eram raramente usadas e afetaram negativamente o desempenho geral do Windows; Como resultado, o recurso foi removido. No Windows 8, esses recursos não estão mais disponíveis:

-   A capacidade de procurar, Pesquisar ou restaurar versões anteriores de arquivos por meio da interface do usuário de versões anteriores
-   A capacidade de configurar ou agendar versões anteriores de arquivos por meio da interface do usuário de proteção do sistema

No entanto, os usuários ainda podem usar a guia versões anteriores ao acessar compartilhamentos de arquivos em um Windows Server.

## <a name="manifestation"></a>Manifestação

A opção de versões anteriores não está mais disponível para volumes locais no menu de propriedades do Windows Explorer.

## <a name="solution"></a>Solução

Os desenvolvedores que precisam criar cópias de sombra de volumes locais ainda podem fazer isso chamando APIs VSS em código personalizado.

 

 




