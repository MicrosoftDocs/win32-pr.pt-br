---
description: A interface ISCardLocate fornece serviços para localizar um cartão inteligente por seu nome.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interface ISCardLocate (Scardmgr. h)
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
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748465"
---
# <a name="iscardlocate-interface"></a>Interface ISCardLocate

\[A interface **ISCardLocate** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **ISCardLocate** fornece serviços para localizar um [*cartão inteligente*](../secgloss/s-gly.md) por seu nome.

Essa interface pode exibir a interface do [*usuário*](../secgloss/u-gly.md) do cartão inteligente, se necessário.

O cenário a seguir mostra um uso típico da interface **ISCardLocate** . A interface **ISCardLocate** é usada para criar uma APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ).

**Para localizar um cartão específico usando seu nome**

1.  Crie uma interface **ISCardLocate** .
2.  Chame [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para procurar um nome de cartão inteligente.
3.  Chame [**FindCard**](iscardlocate-findcard.md) para pesquisar o cartão inteligente.
4.  Interpretar os resultados.
5.  Libere a interface **ISCardLocate** .

## <a name="members"></a>Membros

A interface **ISCardLocate** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardLocate** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardLocate** tem esses métodos.



| Método                                                                  | Descrição                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Reservado para uso futuro.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Especifica o nome do cartão a ser usado na pesquisa.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Pesquisa o cartão inteligente e abre uma conexão válida com ele.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate é definido como 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
