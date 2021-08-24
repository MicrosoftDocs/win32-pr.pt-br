---
description: A interface ISCardDatabase fornece os métodos para executar as operações de banco de dados do gerenciador de recursos de cartão inteligente.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interface ISCardDatabase (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a5bdad1db29630dcf029aab4fbc3812cfc83e0c69dab33c31edb73e21b297b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577166"
---
# <a name="iscarddatabase-interface"></a>Interface ISCardDatabase

\[A interface **ISCardDatabase** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A **interface ISCardDatabase** fornece os métodos para executar as [*operações*](../secgloss/s-gly.md) de banco de dados do gerenciador de [*recursos de*](../secgloss/r-gly.md) cartão inteligente. Essas operações incluem a listagem de cartões inteligentes [*conhecidos,*](../secgloss/r-gly.md)leitores e grupos de leitores, além de recuperar as interfaces com suporte por um cartão inteligente e seu [*provedor de serviços primário.*](../secgloss/p-gly.md)

> [!Note]  
> O identificador do provedor de serviços primário é um GUID COM que pode ser usado para insinciar e usar os objetos COM para um cartão específico.

 

O exemplo a seguir mostra um uso típico da interface **ISCardDatabase.** Nesse caso, a interface **ISCardDatabase** é usada para listar todos os cartões inteligentes conhecidos.

**Para enviar uma transação para um cartão específico**

1.  Crie uma **interface ISCardDatabase.**
2.  Chame [**ListCards para**](iscarddatabase-listcards.md) recuperar todos os cartões inteligentes conhecidos com base em uma cadeia de caracteres [*ATR*](../secgloss/a-gly.md) ou suas interfaces com suporte.
3.  Libere a **interface ISCardDatabase.**

## <a name="members"></a>Membros

A interface **ISCardDatabase** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardDatabase** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardDatabase** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Recupera o identificador do provedor de [*serviços primário para*](../secgloss/p-gly.md) um cartão inteligente específico.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Recupera os GUIDs (identificadores de interface) de todas as interfaces com suporte em um cartão inteligente específico.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Recupera todos os nomes de cartão inteligente que corresponderem a um conjunto específico de GUIDs (identificadores de interface) ou uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md).<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Recupera os nomes dos grupos [*de leitores dos*](../secgloss/r-gly.md) que o gerenciador de recursos tem conhecimento.<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | Recupere os nomes dos leitores [*dos quais*](../secgloss/r-gly.md) o gerenciador de recursos tem conhecimento.<br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardDatabase é definido como \_ 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
