---
description: Um patch que não deve mais ser usado pode ser eliminado da sequência de a patch.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Eliminando patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f025c6487293d07df7963514b79f551045398f8d86f51dd7ab98b589a605e762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913516"
---
# <a name="eliminating-patches"></a>Eliminando patches

Um patch que não deve mais ser usado pode ser eliminado da sequência de a patch. Isso impede que o patch seja aplicado quando o aplicativo de destino é aplicado. Isso é diferente de remover um patch que já está aplicado a um aplicativo. Para obter informações sobre como remover patches aplicados, consulte [Removendo patches](removing-patches.md).

**Windows Instalador 3.0 e posterior: **

Os patches que têm a [tabela MsiPatchSequence](msipatchsequence-table.md) podem usar essa tabela para eliminar patches da sequência de a patch. Um patch pode eliminar patches que vêm antes dele na sequência de a patch e substituir as informações desses patches por suas próprias informações. O patch que especifica quais patches eliminar e os patches que estão sendo eliminados deve ter uma tabela MsiPatchSequence que contém informações.

Se os patches eliminados e o patch de substituição não têm [tabelas MsiPatchSequence,](msipatchsequence-table.md) o pacote de patch pode especificar uma lista de patches a serem eliminados da sequência de a patch em sua propriedade [**Resumo**](revision-number-summary.md) do Número de Revisão. Windows O Instalador 3.0 ignorará essa lista se os patches eliminados ou de substituição têm uma tabela MsiPatchSequence.

Quando o pacote de patch contém patches com informações de sequência na tabela [MsiPatchSequence](msipatchsequence-table.md) e alguns patches sem essas informações, o instalador do Windows 3.0 sequencia os patches na ordem descrita na seção a seguir: Patches de [Sequenciamento](sequencing-patches.md).

Por exemplo, Patch1, Patch2 e Patch3 podem ser três patches que não têm a [tabela MsiPatchSequence.](msipatchsequence-table.md) Patch2 pode ser um patch aplicável somente se Patch1 já tiver sido aplicado ao aplicativo. Patch3 pode ser um patch posterior que tem todas as informações em Patch1 e também elimina Patch1 da sequência de a patch. Isso significa que, quando Patch3 é aplicado, o Patch 2 também se torna inaplicável, pois requer Patch1. Todas as informações somente no Patch2 não são entregues ao aplicativo.

**Windows Instalador 2.0:** Sem suporte. O único método disponível é especificar a lista de patches a serem eliminados da sequência de a patch na propriedade [**Resumo do**](revision-number-summary.md) Número de Revisão.

> [!Note]  
> Os autores de patch devem usar as funções [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) para determinar a sequência de patches que realmente são aplicados ao produto porque a eliminação de alguns patches pode renderizar outros patches inaplicáveis.

 

 

 



