---
title: Sondando alterações usando USNChanged
description: As alterações de Active Directory também podem ser obtidas consultando o atributo uSNChanged, que evita as limitações do controle DirSync.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Sondando alterações usando o AD do USNChanged
- USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e062c84fae575f837f45d78be7c92e5e284c1e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823642"
---
# <a name="polling-for-changes-using-usnchanged"></a>Sondando alterações usando USNChanged

O controle DirSync é poderoso e eficiente, mas tem duas limitações significativas:

-   Somente para aplicativos altamente privilegiados: para usar o controle DirSync, um aplicativo deve ser executado em uma conta que tenha o privilégio de **\_ nome do \_ agente \_ de sincronização se** no controlador de domínio. Algumas contas são tão privilegiadas, portanto, um aplicativo que usa o controle DirSync não pode ser executado por usuários comuns.
-   Nenhum escopo de subárvore: o controle DirSync retorna todas as alterações que ocorrem dentro de um contexto de nomenclatura. Um aplicativo interessado apenas em alterações que ocorrem em uma subárvore pequena de um contexto de nomenclatura deve ser alterado por meio de muitas alterações irrelevantes, o que é ineficiente para o aplicativo e para o controlador de domínio.

As alterações de Active Directory também podem ser obtidas consultando o atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) , que evita as limitações do controle DirSync. Essa alternativa não é melhor do que o controle DirSync em todos os aspectos porque envolve a transmissão de todos os atributos quando qualquer atributo é alterado e requer mais trabalho do desenvolvedor de aplicativos para lidar corretamente com determinados cenários de falha. Atualmente, é a melhor maneira de escrever determinados aplicativos de controle de alterações.

Quando um controlador de domínio modifica um objeto, ele define o atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) do objeto como um valor maior do que o valor anterior do atributo **uSNChanged** para esse objeto e maior que o valor atual do atributo **uSNChanged** para todos os outros objetos mantidos nesse controlador de domínio. Como consequência, um aplicativo pode encontrar o objeto alterado mais recentemente em um controlador de domínio encontrando o objeto com o maior valor **uSNChanged** . O segundo objeto alterado mais recentemente em um controlador de domínio terá o segundo maior valor de **uSNChanged** e assim por diante.

O atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) não é replicado, portanto, ler o atributo **uSNChanged** de um objeto em dois controladores de domínio diferentes normalmente fornecerá valores diferentes.

Por exemplo, o atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) pode ser usado para controlar as alterações em uma subárvore S. Primeiro, execute uma "sincronização completa" da subárvore S. suponha que o maior valor de **uSNChanged** para qualquer objeto em s seja U. consulte periodicamente todos os objetos na subárvore S cujo valor de **uSNChanged** é maior que U. A consulta retornará todos os objetos que foram alterados desde a sincronização completa. Defina para o maior **uSNChanged** entre esses objetos alterados e você estará pronto para sondar novamente.

As sutilezas da implementação de um aplicativo de sincronização [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) incluem:

-   Use o atributo **HighestCommittedUsn** de RootDSE para associar seus filtros de [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) . Ou seja, antes de iniciar uma sincronização completa, leia o **HighestCommittedUsn** do controlador de domínio afiliado. Em seguida, execute uma consulta de sincronização completa (usando os resultados paginados) para inicializar o banco de dados. Quando isso for concluído, armazene o valor de **HighestCommittedUsn** lido antes da consulta de sincronização completa; para usar como os limites inferiores do atributo **uSNChanged** para a próxima sincronização. Posteriormente, para executar uma sincronização incremental, leia novamente o atributo **HighestCommittedUsn** RootDSE. Em seguida, consulte os objetos relevantes, usando os resultados paginados, cujo **uSNChanged** é maior do que os limites inferiores do valor de atributo **uSNChanged** salvo da sincronização anterior. Atualize o banco de dados usando essas informações. Ao concluir, atualize os limites inferiores do atributo **uSNChanged** do valor **HighestCommittedUsn** lido antes da consulta de sincronização incremental. Sempre armazene os limites inferiores do valor do atributo **uSNChanged** no mesmo armazenamento que o aplicativo está sincronizando com o conteúdo do controlador de domínio.

    Seguir esse procedimento, em vez de fazer isso com base nos valores de [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) em objetos recuperados, evita que o servidor Examine novamente os objetos atualizados que estão fora do conjunto que é aplicável ao aplicativo.

-   Como [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) é um atributo não replicado, o aplicativo deve ser associado ao mesmo controlador de domínio sempre que for executado. Se ele não puder se associar a esse controlador de domínio, ele deverá aguardar até que ele possa fazer isso, ou afiliado a um novo controlador de domínio e executar uma sincronização completa com esse controlador de domínio. Quando o aplicativo afiliado a um controlador de domínio, ele registra o nome DNS desse controlador de domínio no armazenamento estável, que é o mesmo armazenamento que está mantendo consistente com o conteúdo do controlador de domínio. Em seguida, ele usa o nome DNS armazenado para associar ao mesmo controlador de domínio para sincronizações subsequentes.
-   O aplicativo deve detectar quando o controlador de domínio no qual ele está afiliado no momento foi restaurado do backup, pois isso pode causar inconsistência. Quando o aplicativo afiliado a um controlador de domínio, ele armazena em cache a "ID de invocação" desse controlador de domínio no armazenamento estável, ou seja, o mesmo armazenamento que está mantendo consistente com o conteúdo do controlador de domínio. A "ID de invocação" de um controlador de domínio é um GUID armazenado no atributo **inrevocationid** do objeto de serviço do controlador de domínio. Para obter o nome distinto do objeto de serviço de um controlador de domínio, leia o atributo **dsServiceName** do RootDSE.

    Lembre-se de que, quando o armazenamento estável do aplicativo é restaurado do backup, não há nenhum problema de consistência porque o nome do controlador de domínio, a ID de invocação e os limites inferiores do valor do atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) são armazenados com os dados sincronizados com o conteúdo do controlador de domínio.

-   Use a paginação ao consultar o servidor, tanto as sincronizações completas quanto as incrementais, para evitar a possibilidade de recuperar grandes conjuntos de resultados simultaneamente. Para obter mais informações, consulte [especificando outras opções de pesquisa](specifying-other-search-options.md).
-   Execute consultas baseadas em índice para evitar forçar o servidor a armazenar grandes resultados intermediários ao usar os resultados paginados. Para obter mais informações, consulte [atributos indexados](indexed-attributes.md).
-   Em geral, não use a classificação do lado do servidor dos resultados da pesquisa, o que pode forçar o servidor a armazenar e classificar grandes resultados intermediários. Isso se aplica a Sincronizações completas e incrementais. Para obter mais informações, consulte [especificando outras opções de pesquisa](specifying-other-search-options.md).
-   Manipule nenhuma condição pai normalmente. O aplicativo pode reconhecer um objeto antes de ter reconhecido seu pai. Dependendo do aplicativo, isso pode ou não ser um problema. O aplicativo sempre pode ler o estado atual do pai a partir do diretório.
-   Para lidar com objetos movidos ou excluídos, armazene o atributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) de cada objeto rastreado. O atributo **objectGUID** de um objeto permanece inalterado, independentemente de onde ele é movido por toda a floresta.
-   Para lidar com objetos movidos, execute Sincronizações completas periódicas ou aumente o escopo da pesquisa e filtre alterações não interessantes na extremidade do cliente.
-   Para lidar com objetos excluídos, execute Sincronizações completas periódicas ou execute uma pesquisa separada para objetos excluídos ao executar uma sincronização incremental. Quando você consulta objetos excluídos, recupere o [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) dos objetos excluídos para determinar os objetos a serem excluídos do banco de dados. Para obter mais informações, consulte [recuperando objetos excluídos](retrieving-deleted-objects.md).
-   Lembre-se de que os resultados da pesquisa incluem apenas os objetos e atributos que o chamador tem permissão para ler (com base nos descritores de segurança e nas DACLs nos vários objetos). Para obter mais informações, consulte [efeitos de segurança em consultas](effects-of-security-on-queries.md).

Para obter mais informações e um exemplo de código que mostra os conceitos básicos de um aplicativo de sincronização USNChanged, consulte [código de exemplo para recuperar alterações usando USNChanged](example-code-to-retrieve-changes-using-usnchanged.md).

 

 