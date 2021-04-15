---
title: Função RtmDeregisterClient (RTM. h)
description: A função RtmDeregisterClient cancela o registro do cliente e libera os recursos associados ao cliente.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- Função RtmDeregisterClient RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369605"
---
# <a name="rtmderegisterclient-function"></a>Função RtmDeregisterClient

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmDeregisterClient** cancela o registro do cliente e libera os recursos associados ao cliente.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientHandle* \[ no\]
</dt> <dd>

Identificador que identifica o cliente para cancelar o registro. Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_identificador inválido do erro \_**</dt> </dl>       | O parâmetro *ClientHandle* não é um identificador válido.<br/> |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Recursos insuficientes para realizar a operação.<br/>  |



 

## <a name="remarks"></a>Comentários

Essa função remove todas as rotas que foram adicionadas pelo cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





