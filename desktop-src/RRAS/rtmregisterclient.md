---
title: Função RtmRegisterClient (RTM. h)
description: A função RtmRegisterClient registra um cliente como um manipulador do protocolo especificado. Ele estabelece um mecanismo de notificação de alteração de rota para o cliente e define as opções de protocolo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- Função RtmRegisterClient RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645052"
---
# <a name="rtmregisterclient-function"></a>Função RtmRegisterClient

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmRegisterClient** registra um cliente como um manipulador do protocolo especificado. Ele estabelece um mecanismo de notificação de alteração de rota para o cliente e define as opções de protocolo.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolFamily* \[ no\]
</dt> <dd>

Especifica a família de protocolos do protocolo de roteamento a ser registrado.

</dd> <dt>

*RoutingProtocol* \[ no\]
</dt> <dd>

Especifica o identificador do protocolo de roteamento, o mesmo usado durante o registro com o Gerenciador do roteador. Consulte [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ no\]
</dt> <dd>

Especifica que uma melhor rota para uma rede na tabela foi alterada. O Gerenciador de tabela de roteamento sinaliza esse evento após uma alteração na melhor rota para qualquer rede na tabela. Consulte [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) para obter mais informações sobre a notificação de alteração de rota.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, o Gerenciador de tabela de roteamento não notificará o cliente sobre as alterações no melhor status de rota.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Especifica opções diversas para tratamento especial do protocolo de roteamento. No momento, há suporte para o seguinte valor.



| Flags                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**\_ \_ rota única do protocolo RTM \_**</dt> </dl> | O Gerenciador de tabela de roteamento mantém apenas uma rota por rede de destino para o protocolo de roteamento. Em outras palavras, o Gerenciador de tabela de roteamento substitui as entradas de rota que têm os mesmos números de rede de destino em vez de adicionar novas.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

No retorno bem-sucedido, um valor de **identificador** que identifica o cliente em chamadas subsequentes para o Gerenciador de tabela de roteamento.

Um identificador **nulo** indica que o Gerenciador de tabelas de roteamento não pôde registrar o cliente. Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o motivo da falha.



| Valor                                                                                                         | Descrição                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**o \_ cliente de erro \_ já \_ existe**</dt> </dl> | Outro cliente já se registrou para manipular o protocolo especificado.<br/>              |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>      | A família de protocolos especificada não tem suporte ou o parâmetro *flags* é inválido.<br/> |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl>   | Recursos insuficientes para realizar a operação.<br/>                                   |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl>     | Memória insuficiente para alocar estruturas de dados para o cliente.<br/>                      |



 

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

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificadores da família de protocolos RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

