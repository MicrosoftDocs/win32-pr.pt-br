---
description: Um patch que não deve mais ser usado pode ser eliminado da sequência de aplicação de patch.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Eliminando patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748987"
---
# <a name="eliminating-patches"></a>Eliminando patches

Um patch que não deve mais ser usado pode ser eliminado da sequência de aplicação de patch. Isso impede que o patch seja aplicado quando o aplicativo de destino é corrigido. Isso é diferente de remover um patch que já está aplicado a um aplicativo. Para obter informações sobre como remover patches aplicados, consulte [removendo patches](removing-patches.md).

* * Windows Installer 3,0 e posterior: * *

Os patches que têm a tabela [MsiPatchSequence](msipatchsequence-table.md) podem usar essa tabela para eliminar patches da sequência de aplicação de patch. Um patch pode eliminar os patches que estão antes dele na sequência de aplicação de patch e substituir as informações desses patches por suas próprias informações. O patch que especifica quais patches devem ser eliminados e os patches que estão sendo eliminados deve ter uma tabela MsiPatchSequence que contém informações.

Se os patches eliminados e o patch de substituição não tiverem tabelas [MsiPatchSequence](msipatchsequence-table.md) , o pacote de patch poderá especificar uma lista de patches a serem eliminados da sequência de aplicação de patch em sua propriedade [**Summary de número de revisão**](revision-number-summary.md) . Windows Installer 3,0 ignora essa lista se os patches eliminados ou de substituição tiverem uma tabela MsiPatchSequence.

Quando o pacote de patch contém patches com informações de sequência na tabela [MsiPatchSequence](msipatchsequence-table.md) e alguns patches sem essas informações, o Windows Installer 3,0 sequencia os patches na ordem descrita na seção a seguir: [patches de sequenciamento](sequencing-patches.md).

Por exemplo, Patch1, Patch2 e Patch3 podem ser três patches que não têm a tabela [MsiPatchSequence](msipatchsequence-table.md) . Patch2 pode ser um patch aplicável somente se o Patch1 já tiver sido aplicado ao aplicativo. Patch3 pode ser um patch posterior que tem todas as informações em Patch1 e também elimina Patch1 da sequência de patches. Isso significa que, quando Patch3 é aplicado, o patch 2 também se torna inaplicável, pois requer Patch1. Todas as informações no Patch2 sozinho não são entregues ao aplicativo.

**Windows Installer 2,0:** Sem suporte. O único método disponível é especificar a lista de patches a serem eliminados da sequência de aplicação de patch na propriedade [**Summary do número de revisão**](revision-number-summary.md) .

> [!Note]  
> Os autores de patch devem usar as funções [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) para determinar a sequência de patches que realmente são aplicados ao produto, pois a eliminação de alguns patches pode renderizar outros patches inaplicável.

 

 

 



