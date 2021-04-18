---
description: Um terminal multitrack pode ser considerado como um terminal que é uma coleção de outros terminais. Cada terminal filho (um &\# 0034; track&\# 0034;) pode ser um terminal multitrack ou um terminal de controle único.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Sobre terminais multitrack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760688"
---
# <a name="about-multitrack-terminals"></a>Sobre terminais multitrack

Um terminal multitrack pode ser considerado como um terminal que é uma coleção de outros terminais. Cada terminal filho (uma "faixa") pode ser um terminal multitrack ou um terminal de controle único.

Todos os terminais multitrack expõem a interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que inclui métodos genéricos para enumerar, criar e remover terminais de faixa de um terminal multitrack. Todos os terminais, controle único e multitrack, expõem a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

Um cliente que tem um ponteiro para uma interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) pode descobrir se o terminal é multitrack ou de controle único consultando o terminal para a interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que é exposta apenas em terminais multitrack.

O terminal pai pode usar a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de seus terminais de faixa ou pode exigir que os terminais de faixa exponham interfaces privadas.

Para obter mais informações, consulte [Track Terminals](track-terminals.md).

 

 
