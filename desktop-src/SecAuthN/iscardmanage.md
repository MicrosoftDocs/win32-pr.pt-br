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
ms.openlocfilehash: cce31ea21701c098b09a0bd96360afb374a9bccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171247"
---
# <a name="iscardmanage-interface"></a>Interface ISCardManage

\[A interface **ISCardManage** não está mais disponível para uso a partir do windows Server 2008, Windows Vista e windows Server 2003 com Service Pack 1 (SP1) e posterior. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviço*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) .

A interface **ISCardManage** deve ser fornecida. Ele é usado para anexar a um [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md)específico, para criar outras interfaces opcionais para executar funções de cartão inteligente específicas, para bloquear um cartão inteligente específico para uso exclusivo e para obter o status de um cartão inteligente ou leitor. Como um conjunto, esses serviços podem ser responsáveis por manter um contexto bem definido no qual um aplicativo possa se comunicar com um [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md).

Veja a seguir um uso típico da interface **ISCardManage** .

**Para se conectar a um cartão inteligente**

1.  Crie a interface **ISCardManage** associada ao cartão.
2.  Conecte-se a um cartão inteligente anexando a um leitor de cartão inteligente específico ([**AttachByIFD**](iscardmanage-attachbyifd.md)) ou usando um identificador anteriormente adquirido ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Crie outras interfaces para executar operações de cartão inteligente ([**CreateCardAuth**](iscardmanage-createcardauth.md), [**createfileaccess**](iscardmanage-createfileaccess.md), [**CreateCHVerification**](iscardmanage-createchverification.md)ou [**createinterface**](iscardmanage-createinterface.md)).
4.  Liberar o cartão ([**desanexar**](iscardmanage-detach.md)).
5.  Libere a interface **ISCardManage** e outras, conforme necessário.

## <a name="members"></a>Membros

A interface **ISCardManage** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardManage** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardManage** tem esses métodos.



| Método                                                            | Descrição                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Permite que um aplicativo crie um link de comunicação para um cartão inteligente usando um identificador retornado pelo Gerenciador de [*recursos*](../secgloss/r-gly.md)do cartão inteligente.<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Permite que um aplicativo solicite o estabelecimento de um contexto para um leitor específico referenciado com um nome de exibição.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Permite a criação de uma interface [**ISCardAuth**](iscardauth.md) .<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Permite a criação de uma interface [**ISCardVerify**](iscardverify.md) .<br/>                                                                                                                                                                                        |
| [**Createfileaccess**](iscardmanage-createfileaccess.md)         | Permite a criação de uma interface [**ISCardFileAccess**](iscardfileaccess.md) .<br/>                                                                                                                                                                                |
| [**Createinterface**](iscardmanage-createinterface.md)           | Permite a criação de uma interface.<br/>                                                                                                                                                                                                                            |
| [**Detach**](iscardmanage-detach.md)                             | Libera o anexo para um determinado cartão inteligente ou leitor alocado por [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.<br/>                                                                |
| [**Reconectar**](iscardmanage-reconnect.md)                       | Permite que um aplicativo se reconecte a um cartão inteligente ou leitor sem a necessidade de emitir uma [**desanexação**](iscardmanage-detach.md) seguida por [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Bloqueia um cartão inteligente ou leitor conectado para uso exclusivo.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Libera o uso exclusivo do cartão inteligente conectado ou leitor.<br/>                                                                                                                                                                                                   |
| [**Status**](iscardmanage-status.md)                             | Permite que um aplicativo obtenha o status atual do leitor ou do cartão inteligente.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



 

 
