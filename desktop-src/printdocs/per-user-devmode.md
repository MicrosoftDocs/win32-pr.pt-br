---
description: Um usuário pode especificar as configurações de documento padrão para uma impressora. Isso é chamado de DEVMODE por usuário porque afeta apenas os padrões de um usuário específico e as informações de cada impressora são definidas em uma estrutura DEVMODE separada.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731916"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

Um usuário pode especificar as configurações de documento padrão para uma impressora. Isso é chamado de *DEVMODE* por usuário porque afeta apenas os padrões de um usuário específico e as informações de cada impressora são definidas em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) separada.

Para definir o DEVMODE por usuário, chame [**SetPrinter**](setprinter.md) com a estrutura [**PRINTER INFO \_ \_ 2**](printer-info-2.md) ou [**PRINTER INFO \_ \_ 9.**](printer-info-9.md) Para redefinir o DEVMODE por usuário para o PADRÃO GLOBAL [**DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea)chame **SetPrinter** com a estrutura [**PRINTER INFO \_ \_ 8.**](printer-info-8.md)

 

 



