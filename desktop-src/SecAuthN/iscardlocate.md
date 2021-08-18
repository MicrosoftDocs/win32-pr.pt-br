---
description: A interface ISCardLocate fornece serviços para localizar um cartão inteligente por seu nome.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interface ISCardLocate (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70679a2decc62011df70e68c119365bb8a98f7bdb06af6d7989eac18e7c14fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922925"
---
# <a name="iscardlocate-interface"></a>Interface ISCardLocate

\[A **interface ISCardLocate** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A **interface ISCardLocate** fornece serviços para localizar um [*cartão inteligente*](../secgloss/s-gly.md) por seu nome.

Essa interface pode exibir a interface do usuário [*do cartão inteligente,*](../secgloss/u-gly.md) se necessário.

O cenário a seguir mostra um uso típico da interface **ISCardLocate.** A **interface ISCardLocate** é usada para criar uma APDU (unidade de dados de protocolo [*de*](../secgloss/a-gly.md) aplicativo).

**Para localizar um cartão específico usando seu nome**

1.  Crie uma **interface ISCardLocate.**
2.  Chame [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para pesquisar um nome de cartão inteligente.
3.  Chame [**FindCard**](iscardlocate-findcard.md) para pesquisar o cartão inteligente.
4.  Interpretar os resultados.
5.  Libere a **interface ISCardLocate.**

## <a name="members"></a>Membros

A **interface ISCardLocate** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardLocate** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ISCardLocate** tem esses métodos.



| Método                                                                  | Descrição                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Reservado para uso futuro.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Especifica o nome do cartão a ser usado na pesquisa.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Pesquisa o cartão inteligente e abre uma conexão válida com ele.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardLocate é definido como \_ 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
