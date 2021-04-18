---
title: Modos de acesso de armazenamento estruturado
description: Os mecanismos para controlar o acesso simultâneo a um objeto, por vários processos e usuários, são essenciais.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, funções de API, sinalizadores de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755299"
---
# <a name="structured-storage-access-modes"></a>Modos de acesso de armazenamento estruturado

Os mecanismos para controlar o acesso simultâneo a um objeto, por vários processos e usuários, são essenciais. O COM fornece esses mecanismos definindo modos de acesso para objetos de armazenamento e de fluxo. O modo de acesso especificado para um objeto de armazenamento pai é herdado por seus filhos, embora você possa inserir restrições adicionais no armazenamento ou fluxo filho. Um objeto de armazenamento ou fluxo aninhado pode ser aberto no mesmo modo ou em um modo mais restrito do que o de seu pai, mas não pode ser aberto em um modo menos restrito do que o de seu pai.

Você especifica modos de acesso usando os valores listados em [**constantes STGM**](stgm-constants.md). Esses valores servem como sinalizadores a serem passados como argumentos para métodos na interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e funções de API associadas. Normalmente, vários sinalizadores são combinados no parâmetro *grfMode*, usando um booliano **ou** uma operação.

Os sinalizadores se enquadram em seis grupos. Somente um sinalizador de cada grupo pode ser especificado por vez:

-   [Sinalizadores de transação](transaction-flags.md)
-   [Sinalizadores de criação de armazenamento](storage-creation-flags.md)
-   [Sinalizadores de criação temporários](temporary-creation-flags.md)
-   [Sinalizadores de prioridade](priority-flags.md)
-   [Sinalizadores de permissão de acesso](access-permission-flags.md)
-   [Sinalizadores de acesso compartilhado](shared-access-flags.md)

 

 




