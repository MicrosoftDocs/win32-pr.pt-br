---
description: O FRS (serviço de replicação de arquivo) foi preterido no Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: O FRS (serviço de replicação de arquivo) foi preterido no Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088364"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>O FRS (serviço de replicação de arquivo) foi preterido no Windows Server 2008 R2

## <a name="platform"></a>Plataforma

 **Servidores-** Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto do recurso

 **Severidade-** Elevada  
**Frequência-** Elevada  


## <a name="description"></a>Descrição

No Windows Server 2008 R2, o FRS (serviço de replicação de arquivo) não pode ser usado para replicar pastas Sistema de Arquivos Distribuído (DFS) ou dados personalizados (não SYSVOL). Um controlador de domínio do Windows Server 2008 R2 ainda pode usar o FRS para replicar o conteúdo do compartilhamento SYSVOL em um domínio que usa o FRS para replicar o compartilhamento SYSVOL entre controladores de domínio. No entanto, os servidores Windows Server 2008 R2 não podem usar o FRS para replicar o conteúdo de qualquer conjunto de réplicas além do compartilhamento de SYSVOL. O serviço de Replicação do DFS é uma substituição para o FRS e pode ser usado para replicar o conteúdo do compartilhamento SYSVOL, pastas DFS, bem como outros dados personalizados (não SYSVOL). Migre todos os conjuntos de réplicas do FRS não SYSVOL para Replicação do DFS. Também é altamente recomendável que você migre a replicação do compartilhamento SYSVOL do FRS para o Replicação do DFS porque Replicação do DFS é mais robusto, escalonável e tem melhor desempenho de replicação do que o FRS.

## <a name="manifestation"></a>Manifestação

A replicação FRS de dados personalizados interromperá a irreversíveis na atualização in-loco. A única maneira de se recuperar dessa situação seria reinstalar um sistema operacional mais antigo no servidor e reinicializar a replicação do FRS. Os servidores que foram atualizados para o Windows Server 2008 R2 não têm permissão para participar de grupos de replicação do FRS existentes.

## <a name="mitigation-of-impact"></a>Mitigação do impacto

Para evitar problemas que possam ocorrer como resultado dessas alterações, migre conjuntos de replicação do FRS personalizados para Replicação do DFS. O serviço de Replicação do DFS tem muitos benefícios sobre o FRS, incluindo ferramentas de gerenciamento aprimoradas, melhor desempenho e gerenciamento delegado.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Visão geral do FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Replicação do sistema de arquivos distribuído: perguntas frequentes](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guia de Migração de Replicação SYSVOL: Replicação FRS para DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
