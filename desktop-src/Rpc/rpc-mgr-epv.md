---
title: RPC_MGR_EPV (rpcdce. h)
description: O tipo de dados Gerenciador de RPC \_ \_ EPV define um vetor de ponto de entrada de Gerenciador.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644328"
---
# <a name="rpc_mgr_epv"></a>Gerenciador de RPC \_ \_ EPV

O tipo de dados Gerenciador de **RPC \_ \_ EPV** define um vetor de ponto de entrada de Gerenciador.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Membros

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**If-name**
</dt> <dd>

Especifica o nome da interface

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo de retorno**
</dt> <dd>

Especifica o tipo retornado pela função **FunctionName** indicada no arquivo IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**
</dt> <dd>

Especifica o nome da função indicada no arquivo IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**parâmetro-lista**
</dt> <dd>

Especifica os parâmetros indicados para a função **FunctionName** no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O vetor de ponto de entrada do Gerenciador (EPV) é uma matriz de ponteiros de função. A matriz contém ponteiros para as implementações das funções especificadas no arquivo IDL. O número de elementos na matriz é definido como o número de funções especificadas no arquivo IDL. Um aplicativo também pode ter vários EPVs, representando várias implementações das funções especificadas na interface.

O compilador MIDL gera um tipo de dados **EPV** padrão chamado * If-name ***\_ Server \_ EPV**, em que *If-name* especifica o identificador de interface no arquivo IDL. O compilador MIDL inicializa esse **EPV** padrão para conter ponteiros de função para cada um dos procedimentos especificados no arquivo IDL.

Quando o servidor oferece várias implementações da mesma interface, o aplicativo de servidor deve declarar e inicializar uma variável do tipo *If-name * * * \_ Server \_ EPV** para cada implementação da interface. Cada **EPV** deve conter um ponto de entrada (ponteiro de função) para cada procedimento definido no arquivo IDL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h (incluir RPC. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





