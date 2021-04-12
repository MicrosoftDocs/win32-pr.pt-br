---
title: Terminologia de pipe essencial
description: Assim como outros tipos de parâmetros para chamadas de procedimento remotos, os pipes podem ter parâmetros \ in \ ou \ out \.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499121"
---
# <a name="essential-pipe-terminology"></a>Terminologia de pipe essencial

Assim como outros tipos de parâmetros para chamadas de procedimento remotos, os pipes podem ter \[ parâmetros [**de entrada**](/windows/desktop/Midl/in) \] ou \[ [**saída**](/windows/desktop/Midl/out-idl) \] . Como o servidor controla a transferência de dados por meio de um pipe, os pipes com o \[  \] atributo in são considerados para efetuar *pull* de dados para o servidor. Da mesma forma, os pipes de saída *enviam* dados do servidor para o cliente. Os procedimentos que fazem a transferência de dados são chamados de *procedimento de pull* e de *Push*, respectivamente.

O compilador MIDL gera os procedimentos push e pull para o servidor. Além disso, ele gerencia a alocação de buffers de dados na memória. No entanto, o cliente deve fornecer seus próprios procedimentos de push e pull. Ele também deve fornecer um procedimento para alocar os buffers de memória usados pelo pipe. Eles são chamados automaticamente no momento apropriado pelo stub do cliente. O procedimento de alocação geralmente é chamado de procedimento de alocação ou função de alocação.

 

 