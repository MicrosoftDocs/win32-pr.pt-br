---
description: A partir do Windows Installer versão 3,0, os autores de patch podem usar a linha de base do produto armazenada em cache pelo instalador para atender mais facilmente aos aplicativos com patches Delta menores.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Reduzindo o tamanho do patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa365e831ab8685073347dc254bac58269135f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759641"
---
# <a name="reducing-patch-size"></a>Reduzindo o tamanho do patch

A partir do Windows Installer versão 3,0, os autores de patch podem usar a linha de base do produto armazenada em cache pelo instalador para atender mais facilmente aos aplicativos com patches Delta menores. Em muitos casos, um [*patch Delta*](d-gly.md) que fornece informações de serviço para um aplicativo pode ser significativamente menor do que um patch de arquivo completo ou pacote de instalação que fornece as mesmas informações.

**Windows Installer 2,0:** Sem suporte. A partir do Windows Installer 3,0, o instalador salva seletivamente as informações de linha de base sobre os arquivos quando eles são atualizados.

O Windows Installer fornece três métodos de atualização e manutenção de aplicativos: [pequenas atualizações](small-updates.md) [, pequenas atualizações e](minor-upgrades.md) [atualizações importantes](major-upgrades.md). Uma pequena atualização também é conhecida como atualização de QFE (Quick Fix Engineering) e uma atualização secundária também é conhecida como atualização de service pack (SP). Uma atualização principal típica remove um aplicativo anterior e instala um novo aplicativo. Windows Installer pode fornecer informações de serviço para aplicativos como um [pacote de instalação](installation-package.md) (arquivo. msi) ou como um pacote de [patch](patch-packages.md) (arquivo. msp).

Um Windows Installer pacote de patch que fornece informações de serviço para uma atualização pequena ou secundária é geralmente muito menor do que o pacote de instalação equivalente que fornece as mesmas informações de serviço. É recomendável que os pacotes de patch sejam usados para a distribuição de atualizações pequenas e secundárias. É recomendável que um pacote de instalação seja usado para a distribuição de uma atualização principal.

Windows Installer patches (arquivos. msp) podem ser gerados a partir de arquivos completos ou de diferenças de arquivo (também chamadas de deltas de arquivo). Um patch Windows Installer gerado a partir de deltas de arquivo pode ser muito menor do que o patch de arquivo completo equivalente. Todas as versões do Windows Installer podem usar patches de arquivo completo ou patches Delta.

A partir do Windows Installer versão 3,0, o instalador salva seletivamente as informações de linha de base sobre os arquivos quando eles são atualizados. As informações sobre o aplicativo base original (a versão RTM) e a atualização secundária mais recente (service pack) são salvas em um local privado quando o aplicativo é instalado ou recebe uma atualização secundária.

O instalador faz o seguinte para minimizar o tamanho do cache de linha de base:

-   No máximo duas linhas de base são mantidas para cada aplicativo: uma linha de base do arquivo como lançada originalmente (RTM) e uma linha de base do arquivo na atualização secundária mais recente (service pack.)
-   Um arquivo não é adicionado ao cache até que seja corrigido. O cache de linha de base é copiar em gravação.
-   Se o aplicativo nunca tiver sido atualizado, não haverá arquivos no cache de linha de base.
-   Quando a última manutenção do aplicativo era uma atualização secundária (service pack), o aplicativo está em um nível de linha de base e no máximo duas cópias de um arquivo podem estar presentes no computador. Uma cópia do arquivo está no diretório de destino da instalação. A outra cópia pode estar no cache de linha de base RTM.
-   Quando a última manutenção do aplicativo era uma QFE (atualização pequena), o aplicativo não está em um nível de linha de base e, no máximo, três cópias de um arquivo podem estar presentes no computador. A primeira cópia do arquivo está no diretório de destino da instalação. A segunda cópia do arquivo está no cache de linha de base RTM. A última cópia do arquivo está no cache de linha de base mais recente.
-   O cache de linha de base do aplicativo é removido quando o produto é desinstalado.

A partir do Windows Installer versão 3,0, o instalador pode usar o cache de linha de base quando os patches são aplicados ao aplicativo. As informações de linha de base podem ser usadas para aplicar um patch Delta ou para reverter um arquivo para uma versão anterior durante uma desinstalação de patch. Isso pode permitir que os autores de patch se beneficiem de patches Delta menores. Se o instalador descobrir que o patch Delta não pode ser aplicado ao arquivo de destino, o instalador poderá tentar usar um arquivo salvo no cache de linha de base como um ponto de partida. O instalador só realiza Resorts para solicitar a fonte de instalação original depois de tentar todas as possibilidades no cache.

A adesão às seguintes diretrizes pode ajudar os autores de patch a usarem Windows Installer patches da versão 3,0 e o cache de linha de base para criar patches Delta menores:

-   Crie patches que incluam a [tabela MsiPatchSequence](msipatchsequence-table.md). Esta tabela é necessária para usar o cache de linha de base e está disponível a partir do Windows Installer versão 3,0.
-   Não defina a política que impede o cache de linha de base. O valor da política [MaxPatchCacheSize](maxpatchcachesize.md) especifica a porcentagem máxima de espaço em disco que pode ser usada. Se a política MaxPatchCacheSize for definida como 0, nenhum arquivo adicional será salvo no cache de linha de base. Se a política não estiver definida, o padrão é que um máximo de 10% do espaço em disco pode ser usado. Se o tamanho total do cache atingir o percentual máximo de espaço em disco, nenhum arquivo adicional será salvo. A política não afeta os arquivos que já foram salvos. Mesmo quando o Caching está desabilitado, o instalador pode usar caches de linha de base de produtos existentes.
-   Se o primeiro patch aplicado incluir a [tabela MsiPatchSequence](msipatchsequence-table.md), o Caching será habilitado para o aplicativo.
-   Se qualquer patch na transação de serviço não incluir a [tabela MsiPatchSequence](msipatchsequence-table.md), o cache será habilitado para o aplicativo somente se um patch de atualização menor (Service Pack) que inclui a tabela MsiPatchSequence for aplicado com êxito ao produto.
-   Gere o pacote de patch usando ferramentas de criação de patch, como [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md).
-   Sempre direcione patches para a versão RTM do aplicativo ou uma versão de atualização secundária (service pack) do aplicativo. Os destinos especificados na [tabela TargetImages](targetimages-table-patchwiz-dll-.md) do arquivo PCP (Propriedades de criação de patch) devem ser pontos de verificação de produto definidos pelos três primeiros campos da propriedade [**ProductVersion**](productversion.md) .
-   Nunca direcione patches em imagens de atualização pequenas. Os destinos para a criação do patch não devem incluir as imagens anteriores de atualização de atualizações pequenas.

 

 



