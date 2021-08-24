---
description: O FRS (Serviço de Replicação de Arquivos) foi preterido no Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: O FRS (Serviço de Replicação de Arquivos) foi preterido no Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72940d2b73b807d5420aface3096714ac132df2095d154fc7563717c33fa6e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759936"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>O FRS (Serviço de Replicação de Arquivos) foi preterido no Windows Server 2008 R2

## <a name="platform"></a>Plataforma

 **Servidores –** Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto do recurso

 **Severidade –** Alta  
**Frequência –** Alta  


## <a name="description"></a>Descrição

No Windows Server 2008 R2, o FRS (Serviço de Replicação de Arquivos) não pode ser usado para replicar pastas Sistema de Arquivos Distribuído (DFS) ou dados personalizados (não SYSVOL). Um controlador de domínio do Windows Server 2008 R2 ainda pode usar FRS para replicar o conteúdo do compartilhamento SYSVOL em um domínio que usa FRS para replicar o compartilhamento SYSVOL entre controladores de domínio. No entanto, Windows server 2008 R2 não podem usar FRS para replicar o conteúdo de qualquer conjunto de réplicas além do compartilhamento SYSVOL. O Replicação do DFS é uma substituição para FRS e pode ser usado para replicar o conteúdo do compartilhamento SYSVOL, pastas DFS, bem como outros dados personalizados (não SYSVOL). Migre todos os conjuntos de réplicas não SYSVOL FRS para Replicação do DFS. Também recomendamos que você migre a replicação do compartilhamento SYSVOL do FRS para o Replicação do DFS porque o Replicação do DFS é mais robusto, escalonável e tem um melhor desempenho de replicação do que o FRS.

## <a name="manifestation"></a>Manifestação

A replicação de FRS de dados personalizados será irreversível após a atualização in-locar. A única maneira de se recuperar dessa situação seria reinstalar um sistema operacional mais antigo no servidor e reinicializar a replicação FRS. Os servidores que foram atualizados para Windows Server 2008 R2 não têm permissão para participar de grupos de replicação FRS existentes.

## <a name="mitigation-of-impact"></a>Mitigação de impacto

Para evitar problemas que podem ocorrer como resultado dessas alterações, migre conjuntos de replicação FRS personalizados para Replicação do DFS. O Replicação do DFS serviço tem muitos benefícios em relação ao FRS, incluindo ferramentas de gerenciamento aprimoradas, maior desempenho e gerenciamento delegado.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Visão geral do FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Replicação do sistema de arquivos distribuído: perguntas frequentes](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guia de Migração de Replicação SYSVOL: Replicação FRS para DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
