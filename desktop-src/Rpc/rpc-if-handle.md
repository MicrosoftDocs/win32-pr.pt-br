---
title: RPC_IF_HANDLE (rpcdce. h)
description: O RPC \_ se o \_ tipo de dados de identificador declara um identificador de interface.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918913"
---
# <a name="rpc_if_handle"></a>RPC \_ se o \_ identificador

O **RPC \_ se \_** o tipo de dados de identificador declara um identificador de interface.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Comentários

A biblioteca de tempo de execução RPC usa identificadores de interface para acessar a estrutura de dados de especificação de interface. O compilador MIDL cria automaticamente uma estrutura de dados de especificação de interface de cada arquivo IDL e cria uma variável global do tipo RPC \_ se \_ o identificador da especificação da interface.

O compilador MIDL inclui um identificador de interface em cada arquivo de cabeçalho gerado para a interface. As funções que exigem a especificação da interface como um parâmetro mostram um tipo de dados de **RPC, \_ se houver \_ identificador**. A forma de cada nome de identificador de interface é a seguinte:

-   *If-name* \_ ClientIfHandle (para o cliente)
-   *If-name* \_ ServerIfHandle (para o servidor)

A parte *If-name* especifica o identificador de interface no arquivo IDL.

Por exemplo:

Olá \_ ClientIfHandle

Olá \_ ServerIfHandle

> [!Note]  
> O comprimento máximo do nome do identificador de interface é 31 caracteres.

 

Como as \_ partes "ClientIfHandle" e " \_ ServerIfHandle" dos nomes exigem 15 caracteres, o elemento *If-name* não pode ter mais de 16 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h (incluir RPC. h)</dt> </dl> |



 

 





