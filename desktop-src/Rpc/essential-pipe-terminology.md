---
title: Terminologia de pipe essencial
description: Assim como outros tipos de parâmetros para chamadas de procedimento remotos, os pipes podem ter parâmetros \ in \ ou \ out \.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389885f440faa477ab22f2100685e2955cbf9fb7ddc4ffcb6440dc4b6f68e003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930065"
---
# <a name="essential-pipe-terminology"></a>Terminologia de pipe essencial

Assim como outros tipos de parâmetros para chamadas de procedimento remotos, os pipes podem ter \[ parâmetros [**de entrada**](/windows/desktop/Midl/in) \] ou \[ [**saída**](/windows/desktop/Midl/out-idl) \] . Como o servidor controla a transferência de dados por meio de um pipe, os pipes com o \[  \] atributo in são considerados para efetuar *pull* de dados para o servidor. Da mesma forma, os pipes de saída *enviam* dados do servidor para o cliente. Os procedimentos que fazem a transferência de dados são chamados de *procedimento de pull* e de *Push*, respectivamente.

O compilador MIDL gera os procedimentos push e pull para o servidor. Além disso, ele gerencia a alocação de buffers de dados na memória. No entanto, o cliente deve fornecer seus próprios procedimentos de push e pull. Ele também deve fornecer um procedimento para alocar os buffers de memória usados pelo pipe. Eles são chamados automaticamente no momento apropriado pelo stub do cliente. O procedimento de alocação geralmente é chamado de procedimento de alocação ou função de alocação.

 

 