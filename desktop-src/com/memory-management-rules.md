---
title: Regras de gerenciamento de memória
description: Regras de gerenciamento de memória
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084943"
---
# <a name="memory-management-rules"></a>Regras de gerenciamento de memória

O tempo de vida de ponteiros para interfaces é sempre gerenciado por meio dos métodos [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em cada interface com. Para obter mais informações, consulte [regras para gerenciar contagens de referência](rules-for-managing-reference-counts.md).

Para todos os outros parâmetros, é importante aderir a determinadas regras para gerenciar a memória. As regras a seguir se aplicam a todos os parâmetros da interface methodsâ € ", incluindo o retorno valueâ €" que não são passados pelo valor:

-   Os parâmetros in-devem ser alocados e liberados pelo chamador.
-   Os parâmetros out devem ser alocados por um chamado; Eles são liberados pelo chamador usando o alocador de memória de tarefa COM padrão. Consulte [o alocador de memória OLE](the-ole-memory-allocator.md) para obter mais informações.
-   Os parâmetros in/out são alocados inicialmente pelo chamador e, em seguida, liberados e realocados por um chamado, se necessário. Como é verdadeiro para parâmetros de saída, o chamador é responsável por liberar o valor retornado final. O alocador de memória COM padrão deve ser usado.

Nos dois últimos casos, em que uma parte do código aloca a memória e uma parte diferente do código a libera, usar o alocador de COM garante que as duas partes do código estejam usando os mesmos métodos de alocação.

Outra área que precisa de atenção especial é o tratamento de parâmetros de saída e de entrada em condições de falha. Se uma função retornar um código de falha, o chamador normalmente não terá como limpar os parâmetros out ou out. Isso leva às seguintes regras adicionais:

-   No caso de uma condição de erro, os parâmetros devem ser sempre definidos de forma confiável para um valor que será limpo sem nenhuma ação pelo chamador.
-   Todos os parâmetros de ponteiro de saída devem ser definidos explicitamente como **NULL**. Normalmente, eles são passados em um parâmetro ponteiro para ponteiro, mas também podem ser passados como membros de uma estrutura que o chamador aloca e o código chamado é preenchido. A maneira mais simples de garantir que isso seja (em parte) definir esses valores como **NULL** na entrada da função. Essa regra é importante porque promove uma interoperabilidade de aplicativo mais robusta.
-   Em condições de erro, todos os parâmetros de entrada devem ser mantidos sozinhos pelo código chamado (assim, permanecendo no valor para o qual foram inicializados pelo chamador) ou definidos explicitamente, como no caso de retorno de erro de parâmetro out.

Lembre-se de que essas convenções de gerenciamento de memória para aplicativos COM aplicam-se apenas às interfaces públicas e APIsâ €. não há nenhum requisito para que a alocação de memória estritamente interna a um aplicativo COM precise ser feita usando esses mecanismos.

O COM internamente usa RPC (chamadas de procedimento remoto) para se comunicar entre clientes e servidores. Para obter mais informações sobre como gerenciar a memória em stubs de servidor RPC, consulte o tópico [Gerenciamento de memória de stub de servidor](../rpc/server-stub-memory-management.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando a alocação de memória](managing-memory-allocation.md)
</dt> </dl>

 

 