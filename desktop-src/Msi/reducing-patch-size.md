---
description: A partir do Windows Installer versão 3.0, os autores de patch podem usar a linha de base do produto armazenada em cache pelo instalador para ajudar mais facilmente os aplicativos com patches delta menores.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Reduzindo o tamanho do patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9024307ecb0971b02c93036dd0de2aefbe797dcf5645f0f07045c4df8956a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534076"
---
# <a name="reducing-patch-size"></a>Reduzindo o tamanho do patch

A partir do Windows Installer versão 3.0, os autores de patch podem usar a linha de base do produto armazenada em cache pelo instalador para ajudar mais facilmente os aplicativos com patches delta menores. Em muitos casos, um [*patch delta*](d-gly.md) que fornece informações de manutenção para um aplicativo pode ser significativamente menor do que um patch de arquivo completo ou pacote de instalação que fornece as mesmas informações.

**Windows Instalador 2.0:** Sem suporte. A partir do Windows 3.0, o instalador salva seletivamente informações de linha de base sobre arquivos quando eles são atualizados.

Windows O instalador fornece três métodos para atualizar e atender [aplicativos:](small-updates.md)pequenas atualizações, atualizações [secundárias](minor-upgrades.md)e [atualizações principais.](major-upgrades.md) Uma pequena atualização também é conhecida como uma atualização QFE (engenharia de correção rápida), e uma atualização secundária também é conhecida como uma atualização service pack (SP). Uma atualização principal típica remove um aplicativo anterior e instala um novo aplicativo. Windows O instalador pode fornecer informações de manutenção para aplicativos como um pacote de instalação [(arquivo](installation-package.md) .msi) ou como um pacote [de patch](patch-packages.md) (arquivo .msp).

Um pacote de patch do Windows Installer que fornece informações de manutenção para uma pequena atualização ou atualização secundária geralmente é muito menor do que o pacote de instalação equivalente que fornece as mesmas informações de manutenção. É recomendável que os pacotes de patch sejam usados para a distribuição de atualizações pequenas e secundárias. É recomendável que um pacote de instalação seja usado para a distribuição de uma atualização principal.

Windows Os patches do instalador (arquivos .msp) podem ser gerados de arquivos completos ou de diferenças de arquivo (também chamados de deltas de arquivo).) Um Windows patch do Instalador gerado de deltas de arquivo pode ser muito menor do que o patch de arquivo completo equivalente. Todas as versões do Windows Instalador podem usar patches de arquivo completo ou patches delta.

Começando com Windows Installer versão 3.0, o instalador salva seletivamente as informações de linha de base sobre arquivos quando eles são atualizados. As informações sobre o aplicativo base original (a versão RTM) e a atualização secundária mais recente (service pack) são salvas em um local privado quando o aplicativo é instalado ou recebe uma atualização secundária.

O instalador faz o seguinte para minimizar o tamanho do cache de linha de base:

-   Não mais do que duas linhas de base são mantidas para cada aplicativo: uma linha de base do arquivo conforme lançado originalmente (RTM) e uma linha de base do arquivo na atualização secundária mais recente (service pack.)
-   Um arquivo não é adicionado ao cache até que ele seja patchado. O cache de linha de base é copy-on-write.
-   Se o aplicativo nunca tiver sido atualizado, não haverá arquivos no cache de linha de base.
-   Quando a última manutenção do aplicativo foi uma atualização secundária (service pack), o aplicativo está em um nível de linha de base e, no máximo, duas cópias de um arquivo podem estar presentes no computador. Uma cópia do arquivo está no diretório de destino da instalação. A outra cópia pode estar no cache de linha de base RTM.
-   Quando a última manutenção do aplicativo foi uma pequena atualização (QFE), o aplicativo não está em um nível de linha de base e, no máximo, três cópias de um arquivo podem estar presentes no computador. A primeira cópia do arquivo está no diretório de destino da instalação. A segunda cópia do arquivo está no cache de linha de base RTM. A última cópia do arquivo está no cache de linha de base mais recente.
-   O cache de linha de base do aplicativo é removido quando o produto é desinstalado.

Começando com Windows Installer versão 3.0, o instalador pode usar o cache de linha de base quando patches são aplicados ao aplicativo. As informações de linha de base podem ser usadas para aplicar um patch delta ou reverter um arquivo para uma versão anterior durante uma desinstalação de patch. Isso pode permitir que os autores de patch se beneficiem de patches delta menores. Se o instalador descobrir que o patch delta não pode ser aplicado ao arquivo de destino, o instalador poderá tentar usar um arquivo salvo no cache de linha de base como um ponto de partida. O instalador recorre apenas à solicitação da fonte de instalação original depois de tentar todas as possibilidades no cache.

A adesão às diretrizes a seguir pode ajudar os autores de patch a usarem patches Windows Installer versão 3.0 e o cache de linha de base para criar patches delta menores:

-   Patches de autor que incluem a [tabela MsiPatchSequence](msipatchsequence-table.md). Essa tabela é necessária para usar o cache de linha de base e está disponível a partir do Windows Installer versão 3.0.
-   Não de acordo com a política que impede o cache de linha de base. O valor da [política MaxPatchCacheSize](maxpatchcachesize.md) especifica o percentual máximo de espaço em disco que pode ser usado. Se a política MaxPatchCacheSize estiver definida como 0, nenhum arquivo adicional será salvo no cache de linha de base. Se a política não estiver definida, o padrão é que um máximo de 10% do espaço em disco possa ser usado. Se o tamanho total do cache atingir o percentual máximo de espaço em disco, nenhum arquivo adicional será salvo. A política não afeta arquivos que já foram salvos. Mesmo quando o cache é desabilitado, o instalador pode usar caches de linha de base de produto existentes.
-   Se o primeiro patch aplicado incluir a [tabela MsiPatchSequence](msipatchsequence-table.md), o cache será habilitado para o aplicativo.
-   Se qualquer patch na transação de manutenção não incluir a tabela [MsiPatchSequence](msipatchsequence-table.md), o cache será habilitado para o aplicativo somente se um patch de atualização secundária (service pack) que inclui a tabela MsiPatchSequence for aplicado com êxito ao produto.
-   Gere o pacote de patch usando ferramentas de criação de [ patch, comoMsimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md).
-   Sempre direcionar patches para a versão RTM do aplicativo ou uma versão de atualização secundária (service pack) do aplicativo. Os destinos especificados na tabela [TargetImages](targetimages-table-patchwiz-dll-.md) do arquivo PCP (Propriedades de Criação de Patch) devem ser pontos de verificação de produto definidos pelos três primeiros campos da [**propriedade ProductVersion.**](productversion.md)
-   Nunca direcionar patches em imagens de atualização pequenas. Os destinos para criar o patch não devem incluir imagens de atualização pequenas anteriores.

 

 



