---
description: A função VirtualFree desconfirma e libera páginas de acordo com as regras a seguir.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Liberando memória virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789885"
---
# <a name="freeing-virtual-memory"></a>Liberando memória virtual

A função [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) desconfirma e libera páginas de acordo com as seguintes regras:

-   O desconfirma uma ou mais páginas confirmadas, alterando o estado das páginas para reservado. A desconfirmação de páginas libera o armazenamento físico associado às páginas, tornando-a disponível para ser alocada por qualquer processo. Qualquer bloco de páginas confirmadas pode ser deconfirmado.
-   Libera um bloco de uma ou mais páginas reservadas, alterando o estado das páginas para livre. Liberar um bloco de páginas torna o intervalo de endereços reservados disponíveis para ser alocado pelo processo. As páginas reservadas podem ser liberadas apenas liberando todo o bloco que foi reservado inicialmente pelo [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   O desconfirma e libera um bloco de uma ou mais páginas confirmadas simultaneamente, alterando o estado das páginas para livre. O bloco especificado deve incluir todo o bloco inicialmente reservado pelo [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), e todas as páginas devem estar confirmadas no momento.

Depois que um bloco de memória é liberado ou descomprometido, você nunca pode consultá-lo novamente. Todas as informações que podem ter ficado nessa memória são feitas para sempre. A tentativa de ler ou gravar em uma página livre resulta em uma exceção de violação de acesso. Se você precisar de informações, não desconfirme ou Libere memória que contenha essas informações.

Para especificar que os dados em um intervalo de memória não são mais interessantes, chame o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) com a **\_ redefinição de mem**. As páginas não serão lidas ou gravadas no arquivo de paginação. No entanto, o bloco de memória pode ser usado novamente mais tarde.

 

 
