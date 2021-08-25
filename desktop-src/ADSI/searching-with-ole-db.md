---
title: Pesquisando com OLE DB
description: Para clientes de Automação que usam ActiveX ADO (Objetos de Dados) e todos os clientes que não são de Automação, a ADSI fornece um provedor OLE DB que dá suporte a um subconjunto de interfaces de OLE DB consulta.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Pesquisando com OLE DB ADSI
- consulta ADSI , pesquisando com OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969dd544600bdb88b2c01b6b932f101f0b9508d7f3f54cd5e6728fd3e4dd5f6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828366"
---
# <a name="searching-with-ole-db"></a>Pesquisando com OLE DB

Para clientes de Automação que usam ActiveX ADO (Objetos de Dados) e todos os clientes que não são de Automação, a ADSI fornece um provedor OLE DB que dá suporte a um subconjunto de interfaces de OLE DB consulta. O código do cliente que já usa OLE DB interfaces para consultas pode usar as mesmas interfaces para consultar serviços de diretório.

Na implementação OLE DB, um serviço de diretório é exposto como um objeto de Fonte de Dados. Os objetos de Fonte de Dados são fábricas para objetos de sessão e suportam [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) para se conectar ao diretório [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) para criar o objeto de [sessão, IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) para fornecer dados de autenticação ao namespace subjacente e fornecer o comando de consulta e [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) para salvar os dados necessários para criar o objeto de fonte de dados no serviço de diretório subjacente.

**Para executar uma consulta do Active Directory usando OLE DB**

1.  Recupere a [interface IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) do provedor OLE DB aplicativo. No caso do Active Directory, use o identificador de classe **CLSID \_ ADsDSOObject**.
2.  Crie uma matriz [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) de dados de conexão especificando o nome de usuário e a senha.
3.  Consulte a interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) recuperada na Etapa 1 para a interface [IDBProperties.](/previous-versions/windows/desktop/ms719607(v=vs.85))
4.  Chame o [método IDBProperties::SetProperties passando](/previous-versions/windows/desktop/ms723049(v=vs.85)) a [matriz DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) criada na Etapa 2.
5.  Chame o [método IDBInitialize::Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) para estabelecer a conexão com o provedor OLE DB; que é o provedor do Active Directory, nesse caso.
6.  Consulte a interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) para a interface [IDBCreateSession.](/previous-versions/windows/desktop/ms724076(v=vs.85))
7.  Chame o [método IDBCreateSession::CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) solicitando uma nova interface do tipo [IDBCreateCommand.](/previous-versions/windows/desktop/ms711625(v=vs.85))
8.  Chame o [método IDBCreateCommand::CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) para criar uma interface [ICommandText.](/previous-versions/windows/desktop/ms714914(v=vs.85))
9.  Chame o [método ICommandText::SetCommandText.](/previous-versions/windows/desktop/ms709757(v=vs.85)) Passe o dialeto preferencial e o texto do comando de consulta real nesse dialeto. **DbGUID \_ LDAPDialect** ou **DBGUID \_ DBSQL** podem ser usados como dialeto.
10. Chame [ICommand::Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); uma [interface IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) é retornada, que é a interface para o conjunto de resultados.
11. Consulte a interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) para a interface [IColumnsInfo.](/previous-versions/windows/desktop/ms725401(v=vs.85))
12. Chame o [método IColumnsInfo::GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) para recuperar dados de coluna sobre o conjunto de resultados.
13. Preencha uma matriz de estruturas [DBBINDING,](/previous-versions/windows/desktop/ms716845(v=vs.85)) descrevendo ao provedor OLE DB como expor os tipos de dados por coluna ao código do aplicativo. Esta etapa permite que você especifique qual TYPE está contido em uma coluna específica. Além disso, os deslocamentos das colunas, em relação à linha retornada, são definidos aqui em uma base coluna por coluna.
14. Consulte a interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) para a interface [IAccessor.](/previous-versions/windows/desktop/ms719672(v=vs.85))
15. Chame o [método IAccessor::CreateAccessor,](/previous-versions/windows/desktop/ms720969(v=vs.85)) que retorna uma matriz de alças do acessador. Essa matriz é usada para acessar as linhas do conjunto de resultados.
16. Chame [IRowset::GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) passando os alças de linha e o número de linhas a obter.
17. Chame [IRowset::GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) passando uma alça de linha do conjunto retornado na Etapa 16. Um ponteiro bruto para a linha é retornado.

Para obter mais informações sobre a sintaxe de filtro de pesquisa, consulte [Sintaxe de filtro de pesquisa](search-filter-syntax.md).

Para ler os dados de linha não processadas retornados, use a estrutura [DBBINDING,](/previous-versions/windows/desktop/ms716845(v=vs.85)) criada na Etapa 13, computar os deslocamentos de coluna no ponteiro de dados não processado retornado na Etapa 17. Leia a parte de status da coluna para um resultado de recuperação nessa coluna.

Para obter mais informações e um exemplo de código que mostra como pesquisar o Active Directory usando o provedor de OLE DB ADSI, consulte Código de exemplo para usar OLE DB [para pesquisar o Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 