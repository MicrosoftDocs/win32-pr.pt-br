---
title: Pesquisando com OLE DB
description: Para clientes de automação que usam ActiveX Data Objects (ADO) e todos os clientes que não são de automação, a ADSI fornece um provedor de OLE DB que dá suporte a um subconjunto de interfaces de consulta OLE DB.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Pesquisando com OLE DB ADSI
- consulta ADSI, pesquisando com OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641855"
---
# <a name="searching-with-ole-db"></a>Pesquisando com OLE DB

Para clientes de automação que usam ActiveX Data Objects (ADO) e todos os clientes que não são de automação, a ADSI fornece um provedor de OLE DB que dá suporte a um subconjunto de interfaces de consulta OLE DB. O código do cliente que já usa interfaces OLE DB para consultas pode usar as mesmas interfaces para consultar serviços de diretório.

Na implementação de OLE DB, um serviço de diretório é exposto como um objeto de fonte de dados. Os objetos de fonte de dados são fábricas de objetos de sessão e dão suporte a [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) para se conectar ao diretório, [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) para criar o objeto de sessão, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) para fornecer dados de autenticação para o namespace subjacente e fornecer o comando de consulta e [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) para salvar os dados necessários para criar o objeto de fonte de dados para o serviço de diretório subjacente.

**Para executar uma consulta Active Directory usando OLE DB**

1.  Recupere a interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) do provedor de OLE DB. No caso de Active Directory, use o CLSID do identificador de classe **\_ ADsDSOObject**.
2.  Crie uma matriz [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) de dados de conexão especificando o nome de usuário e a senha.
3.  Consulte a interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) recuperada na etapa 1 para a interface [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) .
4.  Chame o método [IDBProperties:: SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) passando na matriz [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) criada na etapa 2.
5.  Chame o método [IDBInitialize:: Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) para estabelecer a conexão com o provedor de OLE DB; Esse é o provedor de Active Directory, nesse caso.
6.  Consulte a interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) para a interface [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) .
7.  Chame o método [IDBCreateSession:: CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) solicitando uma nova interface do tipo [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85)).
8.  Chame o método [IDBCreateCommand:: CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) para criar uma interface [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) .
9.  Chame o método [ICommandText:: SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)) . Passe o dialeto preferencial e o texto do comando de consulta real nesse dialeto. **Dbguid \_ LDAPDialect** ou **dbguid \_ DBSQL** pode ser usado como dialeto.
10. Chame [ICommand:: execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); uma interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) é retornada, que é a interface para o conjunto de resultados.
11. Consulte a interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) para a interface [IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85)) .
12. Chame o método [IColumnsInfo:: GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) para recuperar dados de coluna sobre o conjunto de resultados.
13. Preencha uma matriz de estruturas [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , descrevendo para o provedor de OLE DB como expor os tipos de dados de acordo com a coluna para o código do aplicativo. Esta etapa permite que você especifique qual tipo está contido em uma coluna específica. Além disso, os deslocamentos das colunas, em relação à linha retornada, são definidos aqui em uma base coluna a coluna.
14. Consulte a interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) para a interface [IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85)) .
15. Chame o método [IAccessor:: Createaccesser](/previous-versions/windows/desktop/ms720969(v=vs.85)) , que retorna uma matriz de identificadores de acessador. Essa matriz é usada para acessar as linhas do conjunto de resultados.
16. Chame [IRowset:: GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) passando as alças de linha e o número de linhas a serem obtidas.
17. Chame [IRowset:: GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) passando em um identificador de linha, do conjunto retornado na etapa 16. Um ponteiro bruto para a linha é retornado.

Para obter mais informações sobre a sintaxe do filtro de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).

Para ler os dados de linha não processados retornados, use a estrutura [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , criada na etapa 13, computar os deslocamentos de coluna no ponteiro de dados não processados retornado na etapa 17. Leia a parte de status da coluna para obter um resultado de recuperação nessa coluna.

Para obter mais informações e um exemplo de código que mostra como Pesquisar Active Directory usando o provedor de OLE DB ADSI, consulte [código de exemplo para usar OLE DB para pesquisar Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 