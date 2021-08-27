---
description: o grupo do registro de tabelas Windows Installer contém informações sobre entradas do registro.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Grupo de tabelas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ab4d3447ec727271d53fabe44fee11bf96663170c89a2210d80bb02bd8c7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128967"
---
# <a name="registry-tables-group"></a>Grupo de tabelas do registro

![grupo de tabelas do registro](images/registry.png)

Para obter mais informações sobre este diagrama, consulte a [legenda do diagrama de relação de entidade](entity-relationship-diagram-legend.md).

O instalador tem tabelas específicas para os diferentes tipos de entradas de registro. Ao preencher o grupo de tabelas do registro, é importante tentar minimizar o número de entradas colocadas na [tabela do registro](registry-table.md) e maximizar o uso das outras tabelas específicas do registro. Isso ocorre porque o instalador não pode distinguir entre diferentes tipos de entradas de registro na tabela de registro e não pode usar a lógica interna necessária para aproveitar ao máximo todos os recursos do instalador, como [*anúncios*](a-gly.md). A criação de entradas do registro relacionadas ao COM e ao shell dessa maneira também fornece uma organização mais lógica e pode ajudar a minimizar o registro errôneo de informações do servidor COM.

A figura mostra o grupo de entradas de registro de tabelas, bem como a [tabela de componentes](component-table.md), a [tabela de recursos](feature-table.md)e a tabela de [arquivos](file-table.md). Embora os últimos não estejam diretamente envolvidos no preenchimento do registro, eles são incluídos na figura porque são essenciais para a lógica do grupo de entradas do registro.

O grupo de entradas do registro contém as seguintes tabelas de entradas de registro específicas.

-   A [tabela de extensão](extension-table.md) contém todas as extensões de nome de arquivo que seu aplicativo usa junto com seus recursos e componentes associados.
-   A [tabela de verbo](verb-table.md) associa informações de verbo de comando com as extensões de nome de arquivo listadas na [tabela de extensão](extension-table.md). Isso fornece um link indireto entre o verbo e a tabela de recursos necessários para o anúncio de recursos.
-   A [tabela Typelib](typelib-table.md) fornece informações que o instalador coloca no registro para o registro de bibliotecas de tipos. As entradas da biblioteca de tipos não são gravadas no momento do anúncio. O instalador grava as entradas da biblioteca de tipos no momento em que os componentes associados à biblioteca são instalados.
-   A [tabela MIME](mime-table.md) associa um tipo de contexto MIME a um CLSID ou uma extensão de nome de arquivo. Isso fornece um caminho entre a tabela de recursos e MIME que é necessária para o anúncio de recursos.
-   A [tabela selfreg](selfreg-table.md) fornece as informações necessárias para o registro automático de módulos. O Autoregistro é fornecido pelo instalador somente para compatibilidade com versões anteriores e não é recomendado como um método para popular o registro. no entanto, se houver algum módulo em seu aplicativo que deva se registrar, use a tabela SelfReg.
-   A [tabela de classes](class-table.md) é usada para registrar IDs de classe e outras informações para objetos com. Esta tabela contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto.
-   A [tabela ProgID](progid-table.md) associa IDs de programa com IDs de classe.
-   A [tabela AppID](appid-table.md) é usada para registrar configurações comuns de segurança e configuração para objetos DCOM.
-   a [tabela de ambiente](environment-table.md) é usada para definir os valores de variáveis de ambiente e, no Windows 2000, a tabela de ambiente também grava no registro.
-   A [tabela de registro](registry-table.md) contém outras informações que o aplicativo precisa colocar no registro do sistema. Isso inclui configurações padrão, informações do usuário ou dados ou registro COM sem suporte nas tabelas acima.
-   A [tabela RemoveRegistry](removeregistry-table.md) contém as informações de registro que o aplicativo precisa excluir do registro do sistema no momento da instalação.

 

 



