---
title: Descritor de header de procedimento
description: O header foi estendido várias vezes ao longo da vida útil do mecanismo NDR. O compilador atual ainda gera diferentes headers dependendo do modo do compilador. No entanto, os headers mais recentes são um superconjunto dos mais antigos.
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
# <a name="procedure-header-descriptor"></a>Descritor de header de procedimento

O header foi estendido várias vezes ao longo da vida útil do mecanismo NDR. O compilador atual ainda gera diferentes headers dependendo do modo do compilador. No entanto, os headers mais recentes são um superconjunto dos mais antigos.

## <a name="the-old-oi-header"></a>O antigo –Oi Header

O header tem o seguinte formato:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Em que o tipo<1> pode ser um \_ dos valores mostrados na tabela a seguir.



| Hex | Handle               |
|-----|----------------------|
| 31  | FC \_ BIND \_ GENERIC    |
| 32  | FC \_ BIND \_ PRIMITIVE  |
| 33  | FC \_ AUTO \_ HANDLE     |
| 34  | FC \_ CALLBACK \_ HANDLE |
| 0   | (alça explícita)    |



 

Se o tipo de identificador<1> campo for diferente de zero, o procedimento usará um identificador implícito do \_ tipo indicado. Consulte o [tópico Handles](handles.md) para obter mais informações. Se o tipo de identificador<1> campo for zero, o identificador usado para associação será um dos \_ parâmetros do procedimento.

Os alças explícitos podem ser primitivos, genéricos e de contexto; o último tem o token FC a seguir.



| Hex | Handle            |
|-----|-------------------|
| 30  | CONTEXTO \_ DE FC BIND \_ |



 

Por convenção, o tipo de identificador para interfaces DCOM é FC \_ AUTO \_ HANDLE.

O campo de<1> Oi é uma máscara de \_ 8 bits dos sinalizadores a seguir.



| Hex | Sinalizador                         | Significado                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Oi \_ FULL \_ PTR \_ USED          | Usa o pacote de ponteiro completo.           |
| 02  | Oi \_ RPCSS \_ ALLOC \_ USED       | Usa o pacote de memória RpcSs.           |
| 04  | Oi \_ OBJECT \_ PROC             | Um procedimento em uma interface de objeto.      |
| 08  | OI \_ TEM \_ RPCFLAGS            | O procedimento tem sinalizadores Rpc não zero.     |
| 10  | Oi\_\*                       | Sobrecarregado.                              |
| 20  | Oi\_\*                       | Sobrecarregado.                              |
| 40  | OI \_ USAR \_ NOVAS \_ ROTINAS DE \_ IIT | Usa Windows rotinas de init do NT3.5 Beta2+. |
| 80  |                              | Não utilizado.                                  |



 

Os sinalizadores a seguir estão sobrecarregados.



| Hex | Sinalizador                                    | Significado                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | A \_ CODIFICAÇÃO É \_ USADA                        | Usado somente no selamento.                              |
| 20  | DECODE \_ É \_ USADO                        | Usado somente no selamento.                              |
| 10  | Oi \_ IGNORE TRATAMENTO DE \_ \_ EXCEÇÃO DE \_ OBJETO | Não é mais usado (OLE antigo).                         |
| 20  | OI \_ TEM \_ COMM OU \_ \_ FALHA                | Somente em RPC bruto, \[ comm \_ , status de \_ \] falha.        |
| 20  | Oi \_ OBJ \_ USE \_ INTERPRETADOR V2 \_           | Somente no DCOM, use [**o interpretador –Oif.**](/windows/desktop/Midl/-oi) |



 

Os sinalizadores rpc<4> campo descreve como definir o \_ **campo RpcFlags** da estrutura [**RPC \_ MESSAGE.**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) Esse campo só estará presente se os sinalizadores de Oi \_<1> campo tiver \_ \_ RPCFLAGS Oi HAD definido. Se esse campo não estiver presente, os sinalizadores RPC para o procedimento remoto serão zero.

> [!Note]  
> Para desempenho, os interpretadores assíncronos sempre têm os sinalizadores rpc \_<4> campo presente.

 

O campo proc \_ num<2> fornece o número do procedimento.

O tamanho da pilha<2> fornece o tamanho total de todos os parâmetros na pilha, incluindo qualquer ponteiro \_ e/ou valor de retorno.

A \_ descrição \_ explícita do<> campo é descrita posteriormente neste documento. Esse campo não estará presente se o procedimento usar um alça implícito.

 

 