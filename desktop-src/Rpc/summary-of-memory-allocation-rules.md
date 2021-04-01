---
title: Resumo das regras de alocação de memória
description: A tabela a seguir resume as principais regras relacionadas à alocação de memória.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084727"
---
# <a name="summary-of-memory-allocation-rules"></a>Resumo das regras de alocação de memória

A tabela a seguir resume as principais regras relacionadas à alocação de memória.



| Elemento MIDL                                                                                                                                           | Descrição                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ponteiros de \[ [referência](/windows/desktop/Midl/ref) de nível superior \]                                                                                                                | Deve ser ponteiros não nulos.                                                                                                                                            |
| Valor de retorno da função                                                                                                                                  | Uma nova memória sempre é alocada para valores de retorno de ponteiro.                                                                                                             |
| \[[ponteiro exclusivo](/windows/desktop/Midl/unique), [horizontal](/windows/desktop/Midl/out-idl) \] ou \[ [PTR](/windows/desktop/Midl/ptr), out \]                                                                   | Não permitido pelo MIDL.                                                                                                                                                  |
| Ponteiro de nível não \[ [exclusivo](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] ou \[ [PTR](/windows/desktop/Midl/ptr), in e out \] que muda de NULL para não NULL | Stubs de cliente alocam nova memória no cliente no retorno.                                                                                                                 |
| Ponteiro de saída exclusivo de nível não superior \[ [](/windows/desktop/Midl/unique), para [fora](/windows/desktop/Midl/out-idl) , [](/windows/desktop/Midl/in) \] que muda de não nulo para nulo                                 | A memória está órfã no cliente; o aplicativo cliente é responsável por liberar memória e evitar vazamentos.                                                              |
| Ponteiro de nível não-alto \[ [](/windows/desktop/Midl/ptr), [entrada](/windows/desktop/Midl/in)e [saída](/windows/desktop/Midl/out-idl) \] que muda de não nulo para nulo                                       | A memória ficará órfã no cliente se não tiver um alias; o aplicativo cliente é responsável por liberar e impedir vazamentos de memória nesse caso.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Ponteiro                                                                                                                           | A camada de aplicativo do cliente geralmente aloca.                                                                                                                           |
| \[Ponteiro para [saída](/windows/desktop/Midl/out-idl) [não nulo](/windows/desktop/Midl/in) \]                                                                                                | Os stubs tentam gravar no armazenamento existente no cliente. Se a **\[ cadeia de caracteres \]** e o tamanho aumentarem além do tamanho alocado no cliente, isso causará um GP-Fault no retorno. |



 

A tabela a seguir resume os efeitos dos principais atributos IDL e ACF no gerenciamento de memória.



| Recurso MIDL                                                                   | Problemas com o cliente                                                                                                                                  | Problemas do servidor                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[alocar](/windows/desktop/Midl/allocate)( \_ nó único) \] , \[ alocar (todos os \_ nós)\]         | Determina se uma ou várias chamadas são feitas nas funções de memória.                                                                         | Igual ao cliente, exceto que a memória privada geralmente pode ser usada para alocar ( \_ nó único) \[ no \] e \[ nos dados de saída \] .               |
| \[alocar (gratuito) \] ou \[ alocar (não \_ livre)\]                                 | (Nenhum; afeta o servidor.)                                                                                                                        | Determina se a memória no servidor é liberada após cada chamada de procedimento remoto.                                            |
| os atributos \[ de matriz [Max \_ são](/windows/desktop/Midl/max-is) \] e o \[ [tamanho \_ é](/windows/desktop/Midl/size-is)\] | (Nenhum; afeta o servidor.)                                                                                                                        | Determina o tamanho da memória a ser alocada.                                                                                    |
| \[[ \_ contagem de bytes](/windows/desktop/Midl/byte-count)\]                                            | O cliente deve alocar o buffer; não alocado ou liberado por stubs de cliente.                                                                           | O atributo de parâmetro de ACF determina o tamanho do buffer alocado no servidor.                                                        |
| \[[habilitar \_ alocação](/windows/desktop/Midl/enable-allocate)\]                                  | Normalmente, nenhum. No entanto, o cliente pode estar usando um ambiente de gerenciamento de memória diferente.                                                     | O servidor usa um ambiente de gerenciamento de memória diferente. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) deve ser usado para alocações. |
| \[[em](/windows/desktop/Midl/in) \] Attribute                                                    | Aplicativo cliente responsável por alocar memória para dados.                                                                                 | Alocado no servidor por stubs.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] Attribute                                             | Alocado no cliente por stubs.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] o ponteiro somente deve ser um ponteiro de \[ [referência](/windows/desktop/Midl/ref) \] ; alocado no servidor por stubs.                       |
| \[[ref](/windows/desktop/Midl/ref) \] Attribute                                                 | A memória referenciada pelo ponteiro deve ser alocada pelo aplicativo cliente.                                                                          | Ponteiros de referência de nível superior e de primeiro nível gerenciados por stubs.                                                                |
| \[[exclusivo](/windows/desktop/Midl/unique) \] Attribute                                           | Não nulo para NULL pode resultar em memória órfãa; NULL para non-null faz com que o stub do cliente chame a [ \_ \_ alocação do usuário MIDL](/windows/desktop/Midl/midl-user-allocate-1). | (Afeta o cliente.)                                                                                                             |
| \[[PTR](/windows/desktop/Midl/ptr) \] Attribute                                                 | (Consulte \[ [exclusivo](/windows/desktop/Midl/unique) \] .)                                                                                                              | (Consulte \[ [exclusivo](/windows/desktop/Midl/unique) \] .)                                                                                             |



 

 

 