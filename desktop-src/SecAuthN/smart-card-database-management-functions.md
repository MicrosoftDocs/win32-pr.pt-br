---
description: Gerencie o banco de dados do cartão inteligente, atualizando o banco de dados usando um contexto do Gerenciador de recursos especificado.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funções de gerenciamento de banco de dados de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297110"
---
# <a name="smart-card-database-management-functions"></a>Funções de gerenciamento de banco de dados de cartão inteligente

As funções a seguir gerenciam o [*banco de dados do cartão inteligente*](../secgloss/s-gly.md), atualizando o banco de dados usando um [*contexto do Gerenciador de recursos*](../secgloss/r-gly.md)especificado.

> [!Note]  
> A segurança do banco de dados é mantida colocando restrições de acesso no banco de dados, em vez de adicionar mecanismos de segurança ao [*subsistema de cartão inteligente*](../secgloss/s-gly.md).

 



| Tópico                                                            | Descrição                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | Adicione um [*leitor*](../secgloss/r-gly.md) a um [*grupo de leitores*](../secgloss/r-gly.md). |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | Remova um cartão inteligente do sistema.                                                                                                                                    |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | Remova um leitor do sistema.                                                                                                                                        |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | Remova um grupo de leitores do sistema.                                                                                                                                  |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | Introduza um novo cartão para o sistema.                                                                                                                                     |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | Introduza um novo leitor para o sistema.                                                                                                                                   |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | Introduza um novo grupo de leitores para o sistema.                                                                                                                             |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | Remover um leitor de um grupo de leitores.                                                                                                                                    |



 

 

 
