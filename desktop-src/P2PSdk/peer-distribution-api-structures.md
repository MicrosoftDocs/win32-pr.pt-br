---
description: O serviço de distribuição de pares da Microsoft dá suporte às seguintes estruturas.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Estruturas de API de distribuição de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750456"
---
# <a name="peer-distribution-api-structures"></a>Estruturas de API de distribuição de pares

O serviço de distribuição de pares da Microsoft dá suporte às seguintes estruturas.



| Estrutura                                                              | Descrição                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ informações básicas do cliente do PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Indica se há ou não muitos clientes baixando simultaneamente o mesmo conteúdo.                                                                                                                                                                                             |
| [**\_marca de conteúdo PEERDIST \_**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Contém uma marca fornecida pelo cliente, que é um valor de entrada para [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent). A marca está associada ao segmento de conteúdo e é usada em APIs de gerenciamento de conteúdo, como [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent). |
| [**\_Opções de publicação PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Contém opções de publicação, incluindo as informações de versão da API e possíveis sinalizadores de opção.                                                                                                                                                                                           |
| [**opções de recuperação de pares \_ \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Contém a versão das informações de conteúdo a serem recuperadas.                                                                                                                                                                                                                                 |
| [**\_informações de status do PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Contém informações sobre o status atual e os recursos do serviço do BranchCache no computador local.                                                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência da API de distribuição de pares](peer-distribution-api-reference.md)
</dt> </dl>

 

 



