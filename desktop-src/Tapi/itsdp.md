---
description: A interface ITSdp fornece métodos para a manipulação de um protocolo de descritor de sessão (SDP, consulte o componente de blob de conferência RFC 2327).
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: Interface ITSdp (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779460"
---
# <a name="itsdp-interface"></a>Interface ITSdp

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITSdp** fornece métodos para a manipulação de um protocolo de descritor de sessão (SDP, consulte o componente de blob de conferência RFC 2327). Ele fornece as seguintes funcionalidades:

-   Fornece acesso a algumas das propriedades que são comuns a toda a mídia. Eles incluem atributos referentes às informações pessoais do criador, à descrição da sessão e à informação do tipo de endereço.
-   Fornece o ponto de partida para acessar as coleções de tempo e mídia por meio de propriedades.

A interface **ITSdp** é criada chamando **QueryInterface** no [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Membros

A interface **ITSdp** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITSdp** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITSdp** tem esses métodos.



| Método                                                    | Descrição                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**obter \_ Descrição**](itsdp-get-description.md)         | Obtém a descrição da sessão.<br/>                                                            |
| [**obter \_ IsValid**](itsdp-get-isvalid.md)                 | Valida o blob SDP para valores de estrutura e de campo.<br/>                                   |
| [**obter \_ MachineAddress**](itsdp-get-machineaddress.md)   | Obtém o endereço do computador do host de origem.<br/>                                        |
| [**obter \_ mediacollection**](itsdp-get-mediacollection.md) | Obtém o ponteiro para a interface [**ITMediaCollection**](itmediacollection.md) da conferência.<br/> |
| [**obter \_ nome**](itsdp-get-name.md)                       | Obtém o nome da sessão.<br/>                                                                   |
| [**obter \_ originador**](itsdp-get-originator.md)           | Obtém o originador da conferência.<br/>                                                              |
| [**obter \_ ProtocolVersion**](itsdp-get-protocolversion.md) | Obtém a versão do protocolo SDP.<br/>                                                           |
| [**obter \_ SessionID**](itsdp-get-sessionid.md)             | Obtém o valor de NTP (protocolo NTP) de 32 bits que serve como o identificador de sessão.<br/> |
| [**obter \_ SessionVersion**](itsdp-get-sessionversion.md)   | Obtém o valor de 32 bits (idealmente NTP) que serve como a versão da sessão.<br/>                  |
| [**obter \_ timecollection**](itsdp-get-timecollection.md)   | Obtém o ponteiro para a interface [**ITTimeCollection**](ittimecollection.md) da conferência.<br/>   |
| [**obter \_ URL**](itsdp-get-url.md)                         | Obtém a URL.<br/>                                                                            |
| [**Getemailnames**](itsdp-getemailnames.md)              | Obtém a matriz de nomes de email e endereços associados ao blob de conferência.<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | Obtém os números de telefone.<br/>                                                                  |
| [**inserir \_ Descrição**](itsdp-put-description.md)         | Define a descrição da sessão.<br/>                                                            |
| [**colocar \_ MachineAddress**](itsdp-put-machineaddress.md)   | Define o endereço do computador do host de origem.<br/>                                        |
| [**colocar \_ nome**](itsdp-put-name.md)                       | Define o nome da sessão.<br/>                                                                   |
| [**inserir \_ originador**](itsdp-put-originator.md)           | Obtém o originador da conferência.<br/>                                                              |
| [**colocar \_ SessionVersion**](itsdp-put-sessionversion.md)   | Define a versão da sessão.<br/>                                                                    |
| [**colocar \_ URL**](itsdp-put-url.md)                         | Define a URL.<br/>                                                                            |
| [**Setemailnames**](itsdp-setemailnames.md)              | Define a matriz de nomes e endereços de email associados ao blob de conferência.<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | Define os números de telefone.<br/>                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

