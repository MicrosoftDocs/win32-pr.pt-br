---
title: Descritor de cabeçalho de procedimento
description: O cabeçalho foi estendido várias vezes ao longo da vida útil do mecanismo de NDR. O compilador atual ainda gera cabeçalhos diferentes dependendo do modo do compilador. No entanto, os cabeçalhos mais recentes são um superconjunto dos mais antigos.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd9572c9a29ea8477f1d06d8786d50f6abf920de140b6d1663c2431b2ad0c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927124"
---
# <a name="procedure-header-descriptor"></a>Descritor de cabeçalho de procedimento

O cabeçalho foi estendido várias vezes ao longo da vida útil do mecanismo de NDR. O compilador atual ainda gera cabeçalhos diferentes dependendo do modo do compilador. No entanto, os cabeçalhos mais recentes são um superconjunto dos mais antigos.

## <a name="the-old-oi-header"></a>O cabeçalho antigo-Oi

O cabeçalho tem o seguinte formato:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Em que \_ tipo de identificador<1> pode ser um dos valores mostrados na tabela a seguir.



| Hex | Handle               |
|-----|----------------------|
| 31  | FC \_ ligar \_ genérico    |
| 32  | \_primitivo de ligação FC \_  |
| 33  | \_identificador auto do FC \_     |
| 34  | \_identificador de retorno de chamada FC \_ |
| 0   | (identificador explícito)    |



 

Se o tipo de identificador \_<1> campo for diferente de zero, o procedimento usará um identificador implícito do tipo indicado. Consulte o tópico [identificadores](handles.md) para obter mais informações. Se o tipo de identificador \_<1> campo for zero, o identificador usado para associação será um dos parâmetros do procedimento.

Identificadores explícitos podem ser primitivos, genéricos e de contexto; a última tem o token de FC a seguir.



| Hex | Handle            |
|-----|-------------------|
| 30  | \_contexto de ligação FC \_ |



 

Por convenção, o tipo de identificador para interfaces DCOM é o \_ identificador auto do FC \_ .

O \_ campo Oi flags<1> é uma máscara de 8 bits dos sinalizadores a seguir.



| Hex | Sinalizador                         | Significado                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Oi \_ \_ PTR completo \_ usado          | Usa o pacote de ponteiro completo.           |
| 02  | A \_ alocação do Oi RPCSS foi \_ \_ usada       | Usa o pacote de memória do RpcSs.           |
| 04  | \_Proc de objeto Oi \_             | Um procedimento em uma interface de objeto.      |
| 08  | Oi \_ tem \_ RPCFLAGS            | O procedimento tem sinalizadores de RPC diferentes de zero.     |
| 10  | Oi\_\*                       | Sobrecarregado.                              |
| 20  | Oi\_\*                       | Sobrecarregado.                              |
| 40  | Oi \_ usar \_ novas \_ \_ rotinas de inicialização | Usa as rotinas Windows NT 3.5 beta2 + init. |
| 80  |                              | Não utilizado.                                  |



 

Os sinalizadores a seguir estão sobrecarregados.



| Hex | Sinalizador                                    | Significado                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | a codificação \_ é \_ usada                        | Usado apenas na escolha.                              |
| 20  | a decodificação \_ é \_ usada                        | Usado apenas na escolha.                              |
| 10  | Oi \_ ignorar \_ \_ manipulação de exceção de objeto \_ | Não é mais usado (OLE antigo).                         |
| 20  | Oi \_ tem \_ comunicação \_ ou \_ falha                | Em somente RPC bruto, \[ comunicação \_ , status de falha \_ \] .        |
| 20  | O \_ \_ \_ \_ interpretador de uso de Oi obj v2           | Somente no DCOM, use o interpretador [**– OIF**](/windows/desktop/Midl/-oi) . |



 

O \_ campo sinalizadores de rpc<4> descreve como definir o campo **RpcFlags** da estrutura [**de \_ mensagens RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) . Este campo só estará presente se os \_ sinalizadores oi<1> campo tiver Oi \_ \_ RPCFLAGS definido. Se esse campo não estiver presente, os sinalizadores de RPC para o procedimento remoto serão zero.

> [!Note]  
> Para o desempenho, os interpretadores assíncronos sempre têm os sinalizadores de RPC \_<4> campo presente.

 

O \_ campo proc num<2> fornece o número do procedimento do procedimento.

O tamanho da pilha \_<2> fornece o tamanho total de todos os parâmetros na pilha, incluindo qualquer ponteiro e/ou valor de retorno.

A descrição explícita do \_ identificador \_<> campo é descrita mais adiante neste documento. Esse campo não estará presente se o procedimento usar um identificador implícito.

 

 