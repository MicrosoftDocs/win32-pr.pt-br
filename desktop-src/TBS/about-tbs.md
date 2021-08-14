---
title: Sobre TBS
description: Um serviço do sistema que permite o compartilhamento transparente dos recursos Trusted Platform Module (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM Base Services TBS , sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4997bf6181a1da7aabaf811d0f1d0cf3e3ca813bb11a8f2d73b3b286e4e5ebde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954444"
---
# <a name="about-tbs"></a>Sobre TBS

O recurso TBS (Serviços Base do TPM) é um serviço do sistema que permite o compartilhamento transparente dos recursos Trusted Platform Module (TPM). Ele compartilha simultaneamente os recursos do TPM entre vários aplicativos no mesmo computador físico, mesmo se esses aplicativos são executados em máquinas virtuais diferentes. Começando com Windows 8 e Windows Server 2012, o TBS vem pré-instalado em todos os sistemas com um TPM.

O Trusted Computing Group (TCG) define um Trusted Platform Module que fornece funções criptográficas projetadas para fornecer confiança na plataforma. Como o TPM é implementado em hardware, ele tem recursos finitos. O TCG também define uma pilha de software que usa esses recursos para fornecer operações confiáveis para o software do aplicativo. No entanto, nenhuma provisão é feita para executar uma implementação do TSS lado a lado com o software do sistema operacional que também pode estar usando recursos do TPM. O recurso TBS resolve esse problema permitindo que cada pilha de software que se comunique com o TBS use a verificação de recursos do TPM para quaisquer outras pilhas de software que possam estar em execução no computador.

A especificação TPM e a especificação TSS (TCG Software Stack) estão disponíveis em [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

O TBS é implementado como um serviço fora do processo que aceita comandos que usam um serviço RPC. Uma biblioteca vinculada dinamicamente apresenta a interface da linguagem C e se comunica com o serviço TBS.

> [!Note]  
> O serviço TBS aceita apenas solicitações RPC do computador local.

 

As principais metas do TBS são:

-   Forneça um compartilhamento eficiente de recursos limitados do TPM, como slots de chave, slots de sessões de autorização e slots de transporte.
-   Forneça acesso priorizado e sincronizado aos recursos do TPM entre várias instâncias de pilhas de software TPM.
-   Forneça o gerenciamento apropriado de recursos do TPM em todos os estados de energia.
-   Impedir que as pilhas de software TPM acessem comandos do TPM que devem ser restritos, devido a limitações de plataforma ou requisitos administrativos.

A ilustração a seguir mostra a relação do TBS com o TPM.

![relação dos tbs no modo de usuário com o tpm no modo kernel](images/tbs-block-diagram-as11601.png)

 

 




