---
description: Manipula uma descrição de conferência textual.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interface ITConferenceBlob (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761822"
---
# <a name="itconferenceblob-interface"></a>Interface ITConferenceBlob

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITConferenceBlob** manipula uma descrição de conferência textual. A interface destina-se a ser independente do formato e da sintaxe da descrição da conferência. Para manipular aspectos específicos da descrição da conferência, o aplicativo deve consultar outra interface. Atualmente, há suporte apenas para descrições de conferências SDP; o aplicativo deve usar **QueryInterface** para [**ITSdp**](itsdp.md) para acessar os vários campos da descrição da conferência SDP. A interface **ITConferenceBlob** é criada chamando **QueryInterface** no [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membros

A interface **ITConferenceBlob** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConferenceBlob** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITConferenceBlob** tem esses métodos.



| Método                                                             | Descrição                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ CharacterSet**](itconferenceblob-get-characterset.md)     | Obtém o indicador de [**\_ \_ conjunto de caracteres de blob**](blob-character-set.md) de se os caracteres de blob estão em ASCII, Unicode e assim por diante.<br/> |
| [**obter \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | Obtém um ponteiro para o blob de conferência.<br/>                                                                                             |
| [**Init**](itconferenceblob-init.md)                              | Inicializa o blob de conferência.<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | Confirma as alterações no blob de conferência.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

