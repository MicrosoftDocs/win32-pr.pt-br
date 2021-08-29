---
description: A partir do Windows 3.0, os autores podem adicionar informações de sequenciamento de patch ao banco de dados do pacote de patch na tabela MsiPatchSequence.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Patches de sequenciamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f61a72c8122f9f3679cf691f88bc3d9bc952732b9d638ca838f9992068b1c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039999"
---
# <a name="sequencing-patches"></a>Patches de sequenciamento

A partir do Windows 3.0, os autores podem adicionar informações de sequenciamento de patch ao banco de dados do pacote de patch na [tabela MsiPatchSequence.](msipatchsequence-table.md) O instalador pode usar essas informações para determinar quais patches são aplicáveis a um pacote de instalação, determinar a melhor sequência de a patch e instalar patches em uma ordem constante, independentemente da ordem em que são fornecidos ao sistema.

**Windows Instalador 2.0:** Sem suporte. Windows As versões do instalador anteriores ao Windows Instalador 3.0 instalam patches na ordem em que são fornecidas ao sistema, independentemente de conterem uma tabela [MsiPatchSequence.](msipatchsequence-table.md)

A seguir, é necessário usar a funcionalidade de sequenciamento de patch.

-   [Pacotes de patch](patch-packages.md) (arquivos .msp) devem ter uma [tabela MsiPatchSequence](msipatchsequence-table.md) contendo informações de sequenciamento. O instalador instala patches que não têm uma tabela MsiPatchSequence na ordem em que são fornecidos ao sistema.
-   Os patches são instalados usando Windows Instalador 3.0 ou posterior.

Windows O instalador versão 3.0 tem as seguintes funções que os aplicativos podem usar para determinar a melhor sequência de aplicação de patch.

-   A [**função MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) pega uma lista de patches e determina em qual sequência eles podem ser aplicados a um produto instalado. Essa função é responsável por todos os patches ou produtos que já foram instalados no sistema.
-   A [**função MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) pega uma lista de patches e determina em qual sequência eles podem ser aplicados a um produto instalado. Essa função não conta para nenhum patche ou produtos que já foram instalados no sistema.

Windows O instalador versão 3.0 pode aplicar vários patches a um produto em uma única instalação de aplicação de patch. O grupo de patches pode conter patches que incluem informações de sequência de patch (uma [tabela MsiPatchSequence)](msipatchsequence-table.md) e patches que não o fazem. O Windows instalador instala os pacotes de patch sem essa tabela na ordem em que eles são fornecidos ao sistema. O instalador conta para pacotes de patch que não têm uma tabela MsiPatchSequence, mas que foram marcados como patches obsoletos ou sobrescrevidos pelo método descrito na seção a seguir.

Quando Windows Installer versão 3.0 instala vários patches, ele segue estas etapas para determinar a sequência na qual os patches individuais são aplicados ao produto:

1.  Patches instalados sem uma [tabela MsiPatchSequence](msipatchsequence-table.md) são colocados na sequência na ordem em que foram aplicados ao produto. O primeiro patch aplicado é colocado primeiro na sequência.
2.  Novos patches sem uma [tabela MsiPatchSequence](msipatchsequence-table.md) são colocados na sequência. Esses patches estão sendo aplicados pela instalação de aplicação de patch atual. Eles são colocados na ordem em que são fornecidos ao sistema e colocados após todos os patches na etapa 1.
3.  Patches obsoletos são eliminados da sequência de patches.
    > [!Note]  
    > Um pacote de patch pode especificar na propriedade [**Resumo do**](revision-number-summary.md) Número de Revisão uma lista explícita de patches obsoletos a serem removidos pelo patch. Essa lista destina-se ao uso pelo Windows Instalador anterior à versão 3.0. Windows O instalador versão 3.0 remove os patches marcados como obsoletos da sequência, somente se os patches não têm a [tabela MsiPatchSequence](msipatchsequence-table.md).

     

4.  O instalador passa pela sequência de a patch e determina quais patches são aplicáveis na sequência determinada. Quando vários patches são aplicados a um produto, cada patch na sequência também transforma o banco de dados de instalação do produto (.msi arquivo). Um patch será aplicável em uma sequência específica somente se sua transformação [](productlanguage.md)de [](upgradecode.md) banco de dados for capaz de pegar o código do produto [,](product-codes.md)a versão [**,**](productversion.md)a linguagem e o código de atualização que resultam da aplicação das transformaçãos de todos os pacotes de [patch](patch-packages.md) anteriores ao banco de dados do produto. O instalador elimina todos os patches inaplicáveis da sequência.
5.  O instalador começa a colocar patches que têm informações de sequenciamento em sua [tabela MsiPatchSequence.](msipatchsequence-table.md) [Patches](minor-upgrades.md) de atualização secundários que têm a tabela MsiPatchSequence são colocados na sequência após os patches que foram sequenciados nas etapas anteriores e na ordem de suas versões de produto mais baixas para as mais altas depois de serem atualizados. Windows Em seguida, o instalador elimina os patches de atualização secundários que são inaplicáveis nesta sequência.
6.  [Patches de](small-updates.md) atualização pequenos destinados a atualizações [secundárias](minor-upgrades.md) com uma [tabela MsiPatchSequence](msipatchsequence-table.md) são atribuídos à versão mais alta do patch de atualização secundária na sequência.
7.  Todos os pequenos [patches](small-updates.md) de atualização que permanecem não atribuídos após as etapas anteriores e que têm a [](minor-upgrades.md) tabela [MsiPatchSequence](msipatchsequence-table.md) são colocados na sequência antes da primeira atualização secundária que tem a tabela MsiPatchSequence e após o banco de dados de instalação do .msi e todos os patches sem a tabela MsiPatchSequence. Windows Em seguida, o instalador elimina todos os patches de atualização pequenos que são inaplicáveis nesta sequência.
8.  Windows O instalador versão 3.0 elimina os patches sobresserados da sequência. Quando um patch sobressede patches que ocorrem anteriormente na sequência de patch, o patch contém todas as correções nos patches anteriores. Os patches anteriores não são mais necessários. O Windows instalador requer as informações na tabela [MsiPatchSequence](msipatchsequence-table.md) para eliminar patches sobresserados.
    > [!Note]  
    > Os patches destinados a sobressaldar um conjunto anterior de patches devem ser criado para sobressaldar os patches anteriores em todas as famílias de patch. [Patches de](small-updates.md) atualização pequenos só podem ser superados por pequenas atualizações. [Atualizações secundárias](minor-upgrades.md) podem ser superadas tanto pequenas atualizações quanto outras pequenas atualizações.

     

9.  [Pequenos patches](small-updates.md) de atualização que carregam [tabelas MsiPatchSequence](msipatchsequence-table.md) são sequenciados em versões do produto de acordo com as informações de sequenciamento em suas tabelas MsiPatchSequence. Isso determina a sequência de a patch final.

Um patch que não deve mais ser usado pode ser eliminado da sequência de a patch. Para obter mais informações sobre como eliminar patches da sequência de a patch, consulte [Eliminando patches](eliminating-patches.md).

Para obter um exemplo de como a tabela [MsiPatchSequence](msipatchsequence-table.md) pode ser usada para aplicar patches na ordem em que eles são autorados, consulte o Exemplo de aplicação de patch [múltipla](multiple-patching-example.md).

 

 



