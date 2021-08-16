---
title: Resumo das regras de alocação de memória
description: A tabela a seguir resume as principais regras relacionadas à alocação de memória.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec50632693ad0df7ff44aa1d2a9a2760b07a2ed1b72a13ac5dc33294569c3484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924697"
---
# <a name="summary-of-memory-allocation-rules"></a>Resumo das regras de alocação de memória

A tabela a seguir resume as principais regras relacionadas à alocação de memória.



| Elemento MIDL                                                                                                                                           | Description                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ponteiros ref \[ [de nível](/windows/desktop/Midl/ref) \] superior                                                                                                                | Deve ser ponteiros não nulos.                                                                                                                                            |
| Valor de retorno da função                                                                                                                                  | A nova memória sempre é alocada para valores de retorno de ponteiro.                                                                                                             |
| \[[unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] ou \[ [ptr](/windows/desktop/Midl/ptr), ponteiro de \] saída                                                                   | Não permitido por MIDL.                                                                                                                                                  |
| Ponteiro de saída não exclusivo de nível \[ [](/windows/desktop/Midl/unique)superior, [em](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) ou \] \[ [ptr,](/windows/desktop/Midl/ptr)in, que muda \] de nulo para não nulo | Os stubs de cliente alocam nova memória no cliente no retorno.                                                                                                                 |
| Ponteiro de saída exclusivo não de nível \[ [](/windows/desktop/Midl/unique)superior, [em](/windows/desktop/Midl/in), [](/windows/desktop/Midl/out-idl) \] que muda de não nulo para nulo                                 | A memória fica órfã no cliente; O aplicativo cliente é responsável por liberar memória e evitar vazamentos.                                                              |
| Ptr não de nível \[ [superior,](/windows/desktop/Midl/ptr) [em](/windows/desktop/Midl/in), [ponteiro de saída](/windows/desktop/Midl/out-idl) que muda de não \] nulo para nulo                                       | A memória ficará órfã no cliente se não tiver um alias; O aplicativo cliente é responsável por liberar e impedir vazamentos de memória nesse caso.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Ponteiros                                                                                                                           | A camada de aplicativo cliente geralmente aloca.                                                                                                                           |
| Não nulo \[ [em](/windows/desktop/Midl/in), [ponteiro de](/windows/desktop/Midl/out-idl) \] saída                                                                                                | Os stubs tentam gravar no armazenamento existente no cliente. Se **\[ a cadeia de \]** caracteres e o tamanho aumentarem além do tamanho alocado no cliente, isso causará uma falha de GP no retorno. |



 

A tabela a seguir resume os efeitos dos atributos chave IDL e ACF no gerenciamento de memória.



| Recurso MIDL                                                                   | Problemas com o cliente                                                                                                                                  | Problemas no servidor                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[allocate](/windows/desktop/Midl/allocate)(nó \_ único) \] , \[ allocate(all \_ nodes)\]         | Determina se uma ou várias chamadas são feitas para as funções de memória.                                                                         | O mesmo que o cliente, exceto que a memória privada geralmente pode ser usada para alocar (nó único) dados de entrada \_ \[ e \] \[ \] saída.               |
| \[allocate(free) \] \[ or allocate(don't \_ free)\]                                 | (Nenhum; afeta o servidor.)                                                                                                                        | Determina se a memória no servidor é liberada após cada chamada de procedimento remoto.                                            |
| os atributos de \[ [matriz max \_ é](/windows/desktop/Midl/max-is) \] e o tamanho \[ [ \_ é](/windows/desktop/Midl/size-is)\] | (Nenhum; afeta o servidor.)                                                                                                                        | Determina o tamanho da memória a ser alocada.                                                                                    |
| \[[contagem de \_ byte](/windows/desktop/Midl/byte-count)\]                                            | O cliente deve alocar o buffer; não alocado ou liberado por stubs de cliente.                                                                           | O atributo de parâmetro ACF determina o tamanho do buffer alocado no servidor.                                                        |
| \[[ \_ habilitar alocar](/windows/desktop/Midl/enable-allocate)\]                                  | Normalmente, nenhum. No entanto, o cliente pode estar usando um ambiente de gerenciamento de memória diferente.                                                     | O servidor usa um ambiente de gerenciamento de memória diferente. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) deve ser usado para alocações. |
| \[[em](/windows/desktop/Midl/in) \] Atributo                                                    | Aplicativo cliente responsável por alocar memória para dados.                                                                                 | Alocado no servidor por stubs.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] Atributo                                             | Alocado no cliente por stubs.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] -only pointer deve ser \[ [ponteiro ref;](/windows/desktop/Midl/ref) \] alocado no servidor por stubs.                       |
| \[[ref](/windows/desktop/Midl/ref) \] Atributo                                                 | A memória referenciada pelo ponteiro deve ser alocada pelo aplicativo cliente.                                                                          | Ponteiros de referência de nível superior e de primeiro nível gerenciados por stubs.                                                                |
| \[[exclusivo](/windows/desktop/Midl/unique) \] Atributo                                           | Não nulo para nulo pode resultar em memória órfã; nulo para não nulo faz com que o stub do cliente chame [o \_ usuário médio \_ alocar](/windows/desktop/Midl/midl-user-allocate-1). | (Afeta o cliente.)                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] Atributo                                                 | (Consulte \[ [unique](/windows/desktop/Midl/unique) \] .)                                                                                                              | (Consulte \[ [unique](/windows/desktop/Midl/unique) \] .)                                                                                             |



 

 

 