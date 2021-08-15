---
title: RPC_IF_HANDLE (Rpcdce.h)
description: O tipo de dados RPC \_ IF HANDLE declara um \_ identificador de interface.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4652fbd08c583ad0a33638e52face9569e6ff701cb6dc2b775c7060134b60437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926435"
---
# <a name="rpc_if_handle"></a>RPC \_ IF \_ HANDLE

O **tipo de dados RPC IF \_ \_ HANDLE** declara um identificador de interface.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Comentários

A biblioteca em tempo de executar RPC usa alças de interface para acessar a estrutura de dados de especificação de interface. O compilador MIDL cria automaticamente uma estrutura de dados de especificação de interface de cada arquivo IDL e cria uma variável global do tipo RPC IF HANDLE para a \_ \_ especificação da interface.

O compilador MIDL inclui um alça de interface em cada arquivo de header gerado para a interface. As funções que exigem a especificação da interface como um parâmetro mostram um tipo de dados **RPC \_ IF \_ HANDLE**. A forma de cada nome de alça de interface é a seguinte:

-   *if-name* \_ ClientIfHandle (para o cliente)
-   *if-name* \_ ServerIfHandle (para o servidor)

A *parte if-name* especifica o identificador de interface no arquivo IDL.

Por exemplo:

hello \_ ClientIfHandle

hello \_ ServerIfHandle

> [!Note]  
> O comprimento máximo do nome do alça de interface é de 31 caracteres.

 

Como as partes " ClientIfHandle" e " ServerIfHandle" dos nomes exigem 15 caracteres, o elemento if-name pode ter no mínimo \_ \_ 16  caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



 

 





