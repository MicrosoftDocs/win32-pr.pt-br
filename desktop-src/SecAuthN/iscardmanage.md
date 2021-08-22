---
description: Usado para anexar a um cartão inteligente ou leitor específico, para criar outras interfaces opcionais para executar funções de cartão inteligente específicas, para bloquear um cartão inteligente específico para uso exclusivo e para obter o status de um cartão inteligente ou leitor.
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: Interface ISCardManage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: c027ae9004a8437f3d182fdef3335c8fbbad67abaab5c15e351520f2ae592818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922645"
---
# <a name="iscardmanage-interface"></a>Interface ISCardManage

\[A interface **ISCardManage** não está mais disponível para uso a partir do Windows Server 2008, Windows Vista e Windows Server 2003 com Service Pack 1 (SP1) e posterior. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A definição de interface a seguir é fornecida como um padrão que pode ser seguido ao desenvolver um provedor [*de serviços*](../secgloss/s-gly.md) de [*cartão inteligente*](../secgloss/c-gly.md).

A **interface ISCardManage** deve ser fornecida. Ele é usado para anexar a um cartão inteligente ou leitor específico [*para*](../secgloss/r-gly.md)criar outras interfaces opcionais para executar funções de cartão inteligente específicas, para bloquear um cartão inteligente específico para uso exclusivo e para obter o status de um cartão inteligente ou leitor. [](../secgloss/s-gly.md) Como um conjunto, esses serviços podem ser responsáveis por manter um contexto bem definido no qual um aplicativo pode se comunicar com um [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor.*](../secgloss/r-gly.md)

A seguir está um uso típico da interface **ISCardManage.**

**Para se conectar a um cartão inteligente**

1.  Crie a interface **ISCardManage** associada ao cartão.
2.  Conexão um cartão inteligente anexando a um leitor de cartão inteligente específico ([**AttachByIFD**](iscardmanage-attachbyifd.md)) ou usando um alça adquirido anteriormente ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Crie outras interfaces para executar operações de cartão inteligente [**(CreateCardAuth,**](iscardmanage-createcardauth.md) [**CreateFileAccess,**](iscardmanage-createfileaccess.md) [**CreateCHVerification**](iscardmanage-createchverification.md)ou [**CreateInterface).**](iscardmanage-createinterface.md)
4.  Libere o cartão ([**Desconectar**](iscardmanage-detach.md)).
5.  Libere a **interface ISCardManage** e outras conforme necessário.

## <a name="members"></a>Membros

A **interface ISCardManage** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardManage** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ISCardManage** tem esses métodos.



| Método                                                            | Descrição                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Permite que um aplicativo crie um link de comunicação para um cartão inteligente usando um handle retornado pelo gerenciador de [*recursos de cartão inteligente*](../secgloss/r-gly.md).<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Permite que um aplicativo solicite o estabelecimento de um contexto para um leitor específico referenciado com um nome de exibição.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Permite a criação de uma [**interface ISCardAuth.**](iscardauth.md)<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Permite a criação de uma [**interface ISCardVerify.**](iscardverify.md)<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | Permite a criação de uma [**interface ISCardFileAccess.**](iscardfileaccess.md)<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | Permite a criação de uma interface.<br/>                                                                                                                                                                                                                            |
| [**Detach**](iscardmanage-detach.md)                             | Libera o anexo para um cartão inteligente ou leitor específico alocado por [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD,**](iscardmanage-attachbyifd.md) respectivamente.<br/>                                                                |
| [**Reconectar**](iscardmanage-reconnect.md)                       | Permite que um aplicativo se reconecte a um cartão inteligente ou leitor sem [**precisar**](iscardmanage-detach.md) emitir um Detach seguido por [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD,**](iscardmanage-attachbyifd.md) respectivamente.<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Bloqueia um cartão inteligente ou leitor conectado para uso exclusivo.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Libera o uso exclusivo do cartão inteligente ou leitor conectado.<br/>                                                                                                                                                                                                   |
| [**Status**](iscardmanage-status.md)                             | Permite que um aplicativo receba o status atual do cartão inteligente ou leitor.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



 

 
