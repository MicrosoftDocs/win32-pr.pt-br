---
description: A interface ITMedia é uma representação de mídia em um protocolo de descritor de sessão (SDP, consulte RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interface ITMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfd1cf7dcf8ef294481a4687dbac950f97b4adede6a6871222292127e6255057
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034636"
---
# <a name="itmedia-interface"></a>Interface ITMedia

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITMedia** é uma representação de mídia em um protocolo de descritor de sessão (SDP, consulte RFC 2327). Essa interface exporta métodos para obter e definir propriedades básicas de mídia, como tipo. Os métodos [**ITMediaCollection:: get \_ Item**](itmediacollection-get-item.md) e [**ITMediaCollection:: Create**](itmediacollection-create.md) criam a interface **ITMedia** .

## <a name="members"></a>Membros

A interface **ITMedia** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITMedia** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITMedia** tem esses métodos.



| Método                                                          | Descrição                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**obter \_ FormatCodes**](itmedia-get-formatcodes.md)             | Obtém a lista de códigos de formato de carga de mídia.<br/>                                          |
| [**obter \_ MediaName**](itmedia-get-medianame.md)                 | Obtém o nome da mídia.<br/>                                                                  |
| [**obter \_ MediaTitle**](itmedia-get-mediatitle.md)               | Obtém o título da mídia.<br/>                                                                 |
| [**obter \_ NumPorts**](itmedia-get-numports.md)                   | Obtém o número de portas necessárias para a sessão.<br/>                                      |
| [**obter \_ StartPort**](itmedia-get-startport.md)                 | Obtém o valor da porta de 16 bits para a primeira porta.<br/>                                        |
| [**obter \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Obtém o protocolo de transporte.<br/>                                                          |
| [**colocar \_ FormatCodes**](itmedia-put-formatcodes.md)             | Define a lista de códigos de formato de carga de mídia.<br/>                                          |
| [**colocar \_ MediaName**](itmedia-put-medianame.md)                 | Define o nome da mídia.<br/>                                                                  |
| [**colocar \_ MediaTitle**](itmedia-put-mediatitle.md)               | Define o título da mídia.<br/>                                                                 |
| [**colocar \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Define o protocolo de transporte.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Define o valor da porta de 16 bits para a primeira porta e o número de portas necessárias para a sessão.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

