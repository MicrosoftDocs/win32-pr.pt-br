---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: O \_ tipo de dados identificador de associação RPC declara um identificador de associação que contém informações que a biblioteca de tempo de execução RPC usa para acessar informações de associação.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645222"
---
# <a name="rpc_binding_handle"></a>\_identificador de associação RPC \_

O tipo de dados **\_ identificador de associação RPC** declara um identificador de associação que contém informações que a biblioteca de tempo de execução RPC usa para acessar informações de associação.


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>Comentários

A biblioteca de tempo de execução usa informações de associação para estabelecer uma relação de cliente-servidor que permite a execução de chamadas de procedimento remoto. Com base no contexto no qual um identificador de associação é criado, ele é considerado um identificador de associação de servidor ou um identificador de associação de cliente.

Um identificador de associação de servidor contém as informações necessárias para um cliente estabelecer uma relação com um servidor específico. Qualquer número de rotinas de tempo de execução da API RPC retorna um identificador de associação de servidor que pode ser usado para fazer uma chamada de procedimento remoto.

Um identificador de associação de cliente não pode ser usado para fazer uma chamada de procedimento remoto. A biblioteca de tempo de execução RPC cria e fornece um identificador de ligação de cliente para um procedimento chamado-Server (também chamado de rotina Server-Manager) como \_ o \_ parâmetro identificador de associação RPC. O identificador de associação de cliente contém informações sobre o cliente de chamada.

As funções ** \* RpcBinding* _ _*e \* RpcNsBinding*_ retornam o código de status RPC \_ S \_ \_ tipo \_ de associação incorreto \_ quando um aplicativo fornece o tipo de identificador de associação incorreto.

Um aplicativo pode compartilhar um único identificador de associação entre vários threads de execução. A biblioteca de tempo de execução RPC gerencia chamadas de procedimento remoto simultâneas que usam um único identificador de associação. No entanto, o aplicativo é responsável pelo controle de simultaneidade de identificador de associação para operações que modificam um identificador de associação. Essas operações incluem as seguintes rotinas:

-   [_ *RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

Por exemplo, se um aplicativo compartilha um identificador de associação entre dois threads de execução e redefine o ponto de extremidade de identificador de associação em um dos threads chamando [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), os resultados são indefinidos. O identificador de associação no outro thread também pode ser redefinido, ou a operação pode falhar ou o processo pode falhar. Um erro comum é liberar um identificador de associação enquanto uma chamada está em andamento; Isso geralmente falha no processo de chamada.

Se você não quiser a simultaneidade, você pode criar um aplicativo que crie uma cópia de um identificador de ligação chamando [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy). Nesse caso, uma operação para o primeiro identificador de ligação não tem nenhum efeito no segundo identificador de ligação.

As rotinas que exigem um identificador de associação como um parâmetro mostram um tipo de dados de **\_ \_ identificador de associação RPC**. Os parâmetros de identificador de associação são passados por valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h (incluir RPC. h)</dt> </dl> |



 

 





