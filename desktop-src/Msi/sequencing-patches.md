---
description: A partir do Windows Installer 3,0, os autores podem adicionar informações de sequenciamento de patch ao banco de dados do pacote de patch na tabela MsiPatchSequence.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Patches de sequenciamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9cbd9aead596abfaeb50d972915bf4d618440d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172164"
---
# <a name="sequencing-patches"></a>Patches de sequenciamento

A partir do Windows Installer 3,0, os autores podem adicionar informações de sequenciamento de patch ao banco de dados do pacote de patch na tabela [MsiPatchSequence](msipatchsequence-table.md) . O instalador pode usar essas informações para determinar quais patches se aplicam a um pacote de instalação, para determinar a melhor sequência de aplicação de patches e para instalar patches em uma ordem constante, independentemente da ordem em que são fornecidos ao sistema.

**Windows Installer 2,0:** Sem suporte. Windows Installer versões anteriores para Windows Installer 3,0 instalar patches na ordem em que são fornecidas para o sistema, independentemente de contiverem uma tabela [MsiPatchSequence](msipatchsequence-table.md) .

Os itens a seguir são necessários para usar a funcionalidade de sequenciamento de patch.

-   Os [pacotes de patch](patch-packages.md) (arquivos. msp) devem ter uma tabela [MsiPatchSequence](msipatchsequence-table.md) que contém informações de sequenciamento. O instalador instala patches que não têm uma tabela MsiPatchSequence na ordem em que são fornecidos para o sistema.
-   Os patches são instalados usando o Windows Installer 3,0 ou posterior.

Windows Installer versão 3,0 tem as seguintes funções que os aplicativos podem usar para determinar a melhor sequência de aplicação de patches.

-   A função [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) usa uma lista de patches e determina em qual sequência eles podem ser aplicados a um produto instalado. Essa função conta para qualquer patch ou produto que já tenha sido instalado no sistema.
-   A função [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) usa uma lista de patches e determina em qual sequência eles podem ser aplicados a um produto instalado. Essa função não conta nenhum patch ou produto que já tenha sido instalado no sistema.

Windows Installer versão 3,0 pode aplicar vários patches a um produto em uma única instalação de aplicação de patch. O grupo de patches pode conter patches que incluem informações de sequência de patches (uma tabela [MsiPatchSequence](msipatchsequence-table.md) ) e patches que não têm. O Windows Installer instala os pacotes de patch sem essa tabela na ordem em que são fornecidos para o sistema. O instalador conta para pacotes de patch que não têm uma tabela MsiPatchSequence, mas que foram marcados como patches obsoletos ou substituídos pelo método descrito na seção a seguir.

Quando Windows Installer versão 3,0 instala vários patches, ele segue estas etapas para determinar a sequência na qual os patches individuais são aplicados ao produto:

1.  Os patches instalados sem uma tabela [MsiPatchSequence](msipatchsequence-table.md) são colocados na sequência na ordem em que foram aplicados ao produto. O primeiro patch que foi aplicado é colocado primeiro na sequência.
2.  Novos patches sem uma [tabela MsiPatchSequence](msipatchsequence-table.md) são colocados na sequência. Esses patches estão sendo aplicados pela instalação de aplicação de patch atual. Eles são colocados na ordem em que são fornecidos ao sistema e colocados após todos os patches na etapa 1.
3.  Patches obsoletos são eliminados da sequência de patches.
    > [!Note]  
    > Um pacote de patch pode especificar na propriedade [**Resumo do número de revisão**](revision-number-summary.md) uma lista explícita de patches obsoletos a serem removidos pelo patch. Esta lista destina-se ao uso por Windows Installer versões anteriores à versão 3,0. Windows Installer versão 3,0 removerá os patches marcados como obsoletos da sequência, somente se os patches não tiverem a [tabela MsiPatchSequence](msipatchsequence-table.md).

     

4.  O instalador percorre a sequência de aplicação de patch e determina quais patches são aplicáveis na sequência determinada. Quando vários patches são aplicados a um produto, cada patch na sequência também transforma o banco de dados de instalação do produto (arquivo. msi). Um patch será aplicável em uma determinada sequência somente se sua transformação de banco de dados for capaz de pegar o [código do produto](product-codes.md), a [**versão**](productversion.md), a [**linguagem**](productlanguage.md)e o [**UpgradeCode**](upgradecode.md) que resultam da aplicação das transformações de todos os [pacotes de patch](patch-packages.md) anteriores ao banco de dados do produto. O instalador elimina qualquer patch inaplicável da sequência.
5.  O instalador começa a colocar patches que têm informações de sequenciamento em sua tabela [MsiPatchSequence](msipatchsequence-table.md) . Os patches de [atualização secundária](minor-upgrades.md) que têm a tabela MsiPatchSequence são colocados na sequência após os patches que foram sequenciados nas etapas anteriores e na ordem de suas versões de produto mais baixas para a mais alta após serem atualizados. Windows Installer, em seguida, elimina os pequenos patches de atualização que são inaplicáveis nessa sequência.
6.  [Pequenos](small-updates.md) patches de atualização destinados a [pequenas atualizações](minor-upgrades.md) com uma tabela [MsiPatchSequence](msipatchsequence-table.md) são atribuídos à versão mais recente do patch de atualização secundária na sequência.
7.  Todos os pequenos patches de [atualização](small-updates.md) que permanecem sem atribuição após as etapas anteriores, e que têm a tabela [MsiPatchSequence](msipatchsequence-table.md) , são colocados na sequência antes da primeira [atualização secundária](minor-upgrades.md) que tem a tabela MsiPatchSequence e após o banco de dados de instalação. msi e quaisquer patches sem a tabela MsiPatchSequence. Windows Installer, em seguida, elimina os pequenos patches de atualização que são inaplicáveis nessa sequência.
8.  Windows Installer versão 3,0 elimina patches substituídos da sequência. Quando um patch substitui os patches que ocorrem anteriormente na sequência de patch, o patch contém todas as correções nos patches anteriores. Os patches anteriores não são mais necessários. O Windows Installer requer as informações na tabela [MsiPatchSequence](msipatchsequence-table.md) para eliminar patches substituídos.
    > [!Note]  
    > Os patches destinados a substituir um conjunto anterior de patches devem ser criados para substituir os patches anteriores em todas as famílias de patches. Os patches de [atualização pequenos](small-updates.md) só podem substituir pequenas atualizações. As [atualizações secundárias](minor-upgrades.md) podem substituir as pequenas atualizações e outras atualizações secundárias.

     

9.  [Pequenos](small-updates.md) patches de atualização que contêm tabelas [MsiPatchSequence](msipatchsequence-table.md) , são seqüenciados em versões do produto de acordo com as informações de sequenciamento em suas tabelas MsiPatchSequence. Isso determina a sequência de patches final.

Um patch que não deve mais ser usado pode ser eliminado da sequência de aplicação de patch. Para obter mais informações sobre como eliminar patches da sequência de patches, consulte [eliminando patches](eliminating-patches.md).

Para obter um exemplo de como a tabela [MsiPatchSequence](msipatchsequence-table.md) pode ser usada para aplicar patches na ordem em que eles são criados, consulte o [exemplo de vários patches](multiple-patching-example.md).

 

 



