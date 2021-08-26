---
title: Função RtmRegisterClient (Rtm.h)
description: A função RtmRegisterClient registra um cliente como um manipulador do protocolo especificado. Ele estabelece um mecanismo de notificação de alteração de rota para o cliente e define opções de protocolo.
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
ms.openlocfilehash: db58fc9457195c2149fd8d34a8a65a6d5085135275e1c878633f64cb742b02cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081036"
---
# <a name="rtmregisterclient-function"></a>Função RtmRegisterClient

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

A **função RtmRegisterClient** registra um cliente como um manipulador do protocolo especificado. Ele estabelece um mecanismo de notificação de alteração de rota para o cliente e define opções de protocolo.

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

*ProtocolFamily* \[ Em\]
</dt> <dd>

Especifica a família de protocolos do protocolo de roteamento a ser registrado.

</dd> <dt>

*RoutingProtocol* \[ Em\]
</dt> <dd>

Especifica o identificador de protocolo de roteamento, o mesmo usado ao registrar com o gerenciador de roteador. Consulte [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ Em\]
</dt> <dd>

Especifica que uma melhor rota para uma rede na tabela foi alterada. O gerenciador de tabela de roteamento sinaliza esse evento após uma alteração para a melhor rota para qualquer rede na tabela. Consulte [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) para obter mais informações sobre a notificação de alteração de rota.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, o gerenciador de tabela de roteamento não notificará o cliente sobre alterações no melhor status de rota.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Especifica opções diversas para tratamento especial do protocolo de roteamento. No momento, há suporte para o valor a seguir.



| Flags                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**ROTA ÚNICA DO PROTOCOLO RTM \_ \_ \_**</dt> </dl> | O gerenciador de tabela de roteamento mantém apenas uma rota por rede de destino para o protocolo de roteamento. Em outras palavras, o gerenciador de tabela de roteamento substitui entradas de rota que têm os mesmos números de rede de destino em vez de adicionar novos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

No retorno bem-sucedido, **um valor HANDLE** que identifica o cliente em chamadas subsequentes para o gerenciador de tabela de roteamento.

Um **alça NULL** indica que o gerenciador de tabela de roteamento não pôde registrar o cliente. Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o motivo da falha.



| Valor                                                                                                         | Descrição                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**O \_ CLIENTE DE ERRO JÁ \_ \_ EXISTE**</dt> </dl> | Outro cliente já se registrou para lidar com o protocolo especificado.<br/>              |
| <dl> <dt>**ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl>      | Não há suporte para a família de protocolos especificada ou o *parâmetro Flags* é inválido.<br/> |
| <dl> <dt>**ERRO \_ NENHUM RECURSO DO \_ \_ SISTEMA**</dt> </dl>   | Recursos insuficientes para executar a operação.<br/>                                   |
| <dl> <dt>**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**</dt> </dl>     | Memória insuficiente para alocar estruturas de dados para o cliente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificadores de família de protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

