---
title: Sobre TBS
description: Um serviço de sistema que permite o compartilhamento transparente dos recursos de Trusted Platform Module (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TBS de serviços base do TPM, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104161783"
---
# <a name="about-tbs"></a>Sobre TBS

O recurso TBS (serviços base do TPM) é um serviço do sistema que permite o compartilhamento transparente dos recursos do Trusted Platform Module (TPM). Ele compartilha simultaneamente os recursos do TPM entre vários aplicativos no mesmo computador físico, mesmo que esses aplicativos sejam executados em máquinas virtuais diferentes. A partir do Windows 8 e do Windows Server 2012, o TBS vem pré-instalado em todos os sistemas com um TPM.

O Trusted Computing Group (TCG) define um Trusted Platform Module que fornece funções criptográficas projetadas para fornecer confiança na plataforma. Como o TPM é implementado no hardware, ele tem recursos finitos. O TCG também define uma pilha de software que utiliza esses recursos para fornecer operações confiáveis para o software do aplicativo. No entanto, nenhum provisionamento é feito para executar uma implementação de TSS lado a lado com o software do sistema operacional que também pode estar usando recursos do TPM. O recurso TBS resolve esse problema habilitando cada pilha de software que se comunica com TBS para usar os recursos do TPM verificando quaisquer outras pilhas de software que possam estar em execução no computador.

A especificação do TPM e a especificação TSS (pilha de software TCG) estão disponíveis em [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

O TBS é implementado como um serviço fora do processo que aceita comandos que usam um serviço RPC. Uma biblioteca vinculada dinamicamente apresenta a interface de linguagem C e se comunica com o serviço TBS.

> [!Note]  
> O serviço TBS aceita apenas solicitações RPC do computador local.

 

Os principais objetivos do TBS são:

-   Fornecer compartilhamento eficiente de recursos limitados do TPM, como slots de chave, slots de sessões de autorização e slots de transporte.
-   Fornecer acesso priorizado e sincronizado aos recursos do TPM entre várias instâncias de pilhas de software do TPM.
-   Forneça o gerenciamento apropriado de recursos do TPM em todos os Estados de energia.
-   Impedir que as pilhas de software do TPM acessem comandos do TPM que devem ser restritos, devido a limitações de plataforma ou requisitos administrativos.

A ilustração a seguir mostra a relação entre o TBS e o TPM.

![relação entre TBS no modo de usuário e o TPM no modo kernel](images/tbs-block-diagram-as11601.png)

 

 




