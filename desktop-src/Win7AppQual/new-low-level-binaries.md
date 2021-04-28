---
description: Novos binários Low-Level
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Novos binários Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088064"
---
# <a name="new-low-level-binaries"></a>Novos binários Low-Level

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -alta  











## <a name="description"></a>Descrição

Para melhorar a eficiência da engenharia interna e melhorar a base para o trabalho futuro, nós realocamos algumas funcionalidades para novos binários de nível baixo. Essa refatoração possibilitará que futuras instalações do Windows forneçam subconjuntos de funcionalidade para reduzir a área da superfície (requisitos de disco e memória, manutenção e superfície de ataque).

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Como um exemplo de funcionalidade que mudamos para binários de nível baixo, kernelbase.dll Obtém a funcionalidade de kernel32.dll e advapi32.dll. Isso significa que o binário existente agora encaminha as chamadas para o novo binário em vez de tratá-los diretamente; o encaminhamento pode ser estático (a tabela de exportação mostra o redirecionamento) ou tempo de execução (a dll tem uma rotina de stub que chama para o novo binário). Isso afetará aplicativos de nível inferior, como aplicativos de segurança e de backup que dependem de APIs e deslocamentos internos.

## <a name="solution"></a>Solução

O único impacto é o código que faz suposições ao tentar examinar a kernel32.dll ou a tabela de exportação de advapi32.dll na memória, como um aplicativo antivírus pode fazer isso. Use APIs publicadas e não os detalhes de sua implementação. Esse é apenas um exemplo de implementação em um detalhe da implementação de uma API.

 

 



