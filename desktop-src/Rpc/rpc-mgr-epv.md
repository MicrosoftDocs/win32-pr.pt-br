---
title: RPC_MGR_EPV (Rpcdce.h)
description: O tipo de dados RPC \_ MGR \_ EPV define um vetor de ponto de entrada do gerenciador.
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
ms.openlocfilehash: 55e40b883192adc53b11f9965f1a92f4637b320d32b5fd6909e2b6d615437a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926290"
---
# <a name="rpc_mgr_epv"></a>RPC \_ MGR \_ EPV

O tipo de dados **RPC \_ MGR \_ EPV** define um vetor de ponto de entrada do gerenciador.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Membros

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**if-name**
</dt> <dd>

Especifica o nome da interface

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo de retorno**
</dt> <dd>

Especifica o tipo retornado pela função **Functionname** indicada no arquivo IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**
</dt> <dd>

Especifica o nome da função indicada no arquivo IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**
</dt> <dd>

Especifica os parâmetros indicados para a **função Functionname** no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O EPV (vetor de ponto de entrada) do gerenciador é uma matriz de ponteiros de função. A matriz contém ponteiros para as implementações das funções especificadas no arquivo IDL. O número de elementos na matriz é definido como o número de funções especificadas no arquivo IDL. Um aplicativo também pode ter vários EPVs, representando várias implementações das funções especificadas na interface .

O compilador MIDL gera um tipo de dados **EPV** padrão chamado *if-name***\_ SERVER \_ EPV,** em que *if-name* especifica o identificador de interface no arquivo IDL. O compilador MIDL inicializa esse **EPV** padrão para conter ponteiros de função para cada um dos procedimentos especificados no arquivo IDL.

Quando o servidor oferece várias implementações da mesma interface, o aplicativo de servidor deve declarar e inicializar uma variável do tipo *if-name*** \_ SERVER \_ EPV** para cada implementação da interface. Cada **EPV** deve conter um ponto de entrada (ponteiro de função) para cada procedimento definido no arquivo IDL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

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

 

 





