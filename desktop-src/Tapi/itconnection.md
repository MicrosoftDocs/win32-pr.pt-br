---
description: A funcionalidade de interface ITConnection é mostrada abaixo.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interface ITConnection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810137"
---
# <a name="itconnection-interface"></a>Interface ITConnection

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITConnection** fornece a seguinte funcionalidade:

-   Fornece acesso ao endereço e às informações de TTL (vida útil) da sessão.
-   Fornece acesso às informações de largura de banda.
-   Habilita a manipulação da chave de criptografia.

A interface **ITConnection** é criada chamando **QueryInterface** no [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Membros

A interface **ITConnection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConnection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITConnection** tem esses métodos.



| Método                                                               | Descrição                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ AddressType**](itconnection-get-addresstype.md)             | Obtém o tipo de endereço.<br/>                                                                                                              |
| [**obter \_ largura de banda**](itconnection-get-bandwidth.md)                 | Obtém o valor da largura de banda.<br/>                                                                                                               |
| [**obter \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Obtém o modificador de largura de banda.<br/>                                                                                                        |
| [**obter o \_ NetworkType**](itconnection-get-networktype.md)             | Obtém o tipo de rede.<br/>                                                                                                              |
| [**obter \_ NumAddresses**](itconnection-get-numaddresses.md)           | Obtém o número de endereços a serem usados para a sessão.<br/>                                                                            |
| [**obter \_ StartAddress**](itconnection-get-startaddress.md)           | Obtém o primeiro endereço a ser usado para a sessão.<br/>                                                                                  |
| [**obter \_ TTL**](itconnection-get-ttl.md)                             | Obtém o escopo [*TTL (vida útil)*](t-tapgloss.md) para transmissões nos endereços.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Obtém a chave de criptografia.<br/>                                                                                                            |
| [**colocar \_ AddressType**](itconnection-put-addresstype.md)             | Define o tipo de endereço.<br/>                                                                                                              |
| [**colocar \_ NetworkType**](itconnection-put-networktype.md)             | Define o tipo de rede.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Define informações de endereço.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Define o valor de largura de banda.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Define a chave de criptografia necessária para descriptografar a sessão ou uma indicação para um mecanismo para obter uma chave utilizável por meios externos.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

