---
title: Visão geral do código
description: A figura a seguir é uma representação conceitual dos blocos de código necessários para implementar o componente do provedor de exemplo ADSI.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Visão geral do código AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc23f4a3a51c33f24748347a2941bc09dbda8bc3bd99d133f99d0377eb0bda90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017717"
---
# <a name="code-overview"></a>Visão geral do código

A figura a seguir é uma representação conceitual dos blocos de código necessários para implementar o componente do provedor de exemplo ADSI. Cada seção é descrita na figura a seguir. Programadores COM experientes podem achar que essa é uma visão geral adequada do componente de provedor de exemplo. Para obter mais informações, consulte [detalhes do código](code-details.md).

![implementação de provedor de exemplo](images/dssmco.png)

Os itens numerados a seguir correspondem aos elementos de bloco na figura.

1.  Carregando a DLL (LibMain. cpp, GUID. cpp). O ponto de entrada para a DLL. Definições de objeto estático de fábrica de classes para os dois objetos de provedor: GUID. cpp contém as definições de CLSID para as implementações dos vários objetos de componente de provedor de exemplo.
2.  Fábrica de classes de objeto de provedor e código de criação (Cprovcf. cpp, Cprov. cpp, Stdfact. cpp). O objeto Provider é o objeto que dá suporte a [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) durante as operações de associação de moniker, conforme discutido em Localizando e ligando no componente de provedor de exemplo.
3.  Associação a um objeto (Getobj. cpp). Esse código chama o analisador para verificar se o ADsPath fornecido está sintaticamente correto e, em seguida, executa qualquer mapeamento necessário do ADsPath para o caminho do serviço de diretório nativo para o item que está sendo criado como um objeto Active Directory. Ele pesquisa a definição de esquema para esse tipo de objeto e preenche as propriedades obrigatórias. Depois de criar o objeto Active Directory, um ponteiro de interface para [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) é recuperado para o chamador.
4.  Analisador para o namespace do provedor (Parse. cpp). Este é o código invocado pelo item 3. O analisador verifica se a cadeia de caracteres ADsPath passada está sintaticamente correta para seu próprio namespace.
5.  Fábrica de classes, criação e enumeração para o objeto de namespace (Cnamcf. cpp, Cnamesp. cpp, Cenumns. cpp). O objeto namespace é um objeto contêiner que pode ser enumerado para localizar todos os objetos de nó raiz para esse namespace.
6.  Fábrica de classes e código de criação para um objeto de Active Directory genérico e fábrica de classes, criação e código de enumeração para um objeto de contêiner ADs genérico (Cgenobj. cpp, Cenumobj. cpp, Common. cpp, Core. cpp). Esse código é executado quando um objeto de Active Directory é criado.
7.  Filtragem e enumeração de VARIAntes (Cenumvar. cpp, Object. cpp). Quando uma coleção de elementos VARIANT de um único tipo é gerenciada no ADSI, esse código é usado.
8.  Globais (Globals. cpp). Palavras-chave de namespace, estruturas de mapeamento de sintaxe de formatos de dados nativos para o tipo de variante de automação ADs são todos definidos aqui.
9.  Empacotamento/desempacotamento de dados (Pack. cpp, Property. cpp, Smpoper. cpp). A conversão de formatos de dados nativos no conjunto com suporte de tipos VARIAntes de automação ocorre quando as propriedades de um objeto são carregadas no cache de propriedades. Outras manipulações especiais de dados devem ser executadas quando as estruturas com ponteiros são copiadas, excluídas ou movidas na memória.
10. Cache de Propriedades (cProps. cpp). Caching propriedades é um recurso do ambiente ADSI. Os métodos [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)e [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) atuam no cache de propriedades.
11. Gerenciamento de memória (Memory. cpp). O uso de um conjunto de funções de memória para alocar e liberar memória permite que o componente de provedor de exemplo controle o uso de memória e pare os vazamentos de memória.
12. Objetos de esquema e gerenciamento (Cschobj. cpp, Cprpobj. cpp, Cclsobj. cpp, Cenumsch. cpp). Isso inclui rotinas para criar, gerenciar e enumerar os objetos de esquema. Isso inclui objetos de classe de esquema, objetos de propriedade e objetos de sintaxe, além de ser capaz de enumerar o objeto de contêiner de classe de esquema.
13. Chamadas específicas do sistema operacional (RegDSAPI. cpp). Isso inclui todas as chamadas que fazem referência ao sistema operacional nativo. Entre outras funções, elas incluem a abertura de funções, o fechamento, a leitura e a modificação de objetos, bem como aqueles que acessam os dados de esquema e de propriedade. O componente de provedor de exemplo aconteceu para simular uma hierarquia de diretório usando o registro. Somente nomes de função devem ser muito interessantes para um gravador de provedor.
14. Implementação de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr. cpp). Esse código acessa os dados da biblioteca de tipos para permitir que os métodos de interface sejam invocados de forma compatível com a automação.

 

 