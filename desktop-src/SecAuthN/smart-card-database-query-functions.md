---
description: Consulte o banco de dados do cartão inteligente. Eles podem fornecer uma lista de cartões inteligentes fornecidos por um usuário específico, as interfaces e o provedor de serviços primário de um cartão específico, os grupos de leitores definidos para o sistema e os leitores em um conjunto de grupos de leitores.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funções de consulta de banco de dados de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170946"
---
# <a name="smart-card-database-query-functions"></a>Funções de consulta de banco de dados de cartão inteligente

As funções a seguir consultam o [*banco de dados do cartão inteligente*](../secgloss/s-gly.md). Eles podem fornecer uma lista de cartões inteligentes fornecidos por um usuário específico, as interfaces e o [*provedor de serviços primário*](../secgloss/p-gly.md) de um cartão específico, os [*grupos de leitores*](../secgloss/r-gly.md) definidos para o sistema e os [*leitores*](../secgloss/r-gly.md) em um conjunto de grupos de leitores.

Ao usar essas funções, você pode consultar o banco de dados completo do cartão inteligente ou pode restringir a pesquisa definindo o [*contexto do Gerenciador de recursos*](../secgloss/r-gly.md). O contexto do Gerenciador de recursos é definido chamando [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) antes de chamar uma função de consulta.

> [!Note]  
> Sem um contexto especificado, algumas informações ainda podem estar inacessíveis devido a restrições de segurança.

 



| Tópico                                                  | Descrição                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Recupere o identificador (GUID) do [*provedor de serviços primário*](../secgloss/p-gly.md) para o cartão fornecido. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Recupere uma lista de cartões introduzidos anteriormente no sistema por um usuário específico.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Recupere os identificadores (GUIDs) das interfaces fornecidas por um determinado cartão.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Recupere uma lista de grupos de leitores que foram introduzidos anteriormente no sistema.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Recupere a lista de leitores em um conjunto de grupos de leitores nomeados.                                                                                                                    |



 

 

 
