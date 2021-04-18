---
description: A interface ITMedia é uma representação de mídia em um protocolo de descritor de sessão (SDP, consulte RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interface ITMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757213"
---
# <a name="itmedia-interface"></a>Interface ITMedia

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

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
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
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

 

