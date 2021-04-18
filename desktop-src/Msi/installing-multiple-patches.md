---
description: A partir do Windows Installer 3,0, vários patches podem ser aplicados a um produto em uma ordem constante, independentemente da ordem em que os patches são fornecidos ao sistema.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Instalando vários patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4edb8d085ede6aee81690bf67bd9c5e19780ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758624"
---
# <a name="installing-multiple-patches"></a>Instalando vários patches

A partir do Windows Installer 3,0, vários patches podem ser aplicados a um produto em uma ordem constante, independentemente da ordem em que os patches são fornecidos ao sistema.

**Windows Installer 2,0:** Sem suporte. Windows Installer versões anteriores à versão 3,0 sempre instalam patches na ordem em que são fornecidos para o sistema.

**Windows Installer 3,0 e posterior:** O instalador pode usar as informações fornecidas na tabela [MsiPatchSequence](msipatchsequence-table.md) para determinar quais patches são aplicáveis ao pacote de Windows Installer e em qual ordem os patches devem ser aplicados. Os aplicativos podem usar as funções [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) e [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) .

A função [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) determina quais patches se aplicam ao pacote de Windows Installer e em qual sequência. A função pode considerar patches substituídos ou obsoletos. Essa função não conta os produtos ou patches que estão instalados no sistema que não estão especificados no conjunto.

A função de sequência [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) pode determinar a melhor sequência de aplicativos para os patches para um produto instalado especificado. Essa função conta para patches que já foram aplicados ao produto, e contas para patches obsoletos e substituídos.

Quando o pacote de patch não tem uma tabela [MsiPatchSequence](msipatchsequence-table.md) , o instalador sempre aplica os patches na ordem em que eles são fornecidos para o sistema.

Quando o pacote de patch contém uma mistura de patches com informações de sequência na tabela [MsiPatchSequence](msipatchsequence-table.md) e alguns patches sem essas informações, o Windows installer versão 3,0 sequencia os patches na ordem descrita na seção a seguir: [patches de sequenciamento](sequencing-patches.md).

Um pacote Windows Installer pode instalar no máximo 127 patches ao instalar ou atualizar um aplicativo. Quando muitas atualizações são necessárias, elas devem ser combinadas e os patches obsoletos anteriores devem ser eliminados da sequência de aplicação de patch.

Um patch que não deve ser usado pode ser eliminado da sequência de aplicação de patch. Isso impede que o patch seja aplicado quando o aplicativo de destino é corrigido. Isso é diferente de remover um patch que já foi aplicado a um aplicativo. Para obter mais informações sobre como eliminar patches da sequência de aplicação de patch, consulte [eliminando patches](eliminating-patches.md). Para obter informações sobre como remover patches aplicados, consulte [removendo patches](removing-patches.md).

Para obter um exemplo de como Windows Installer aplica vários patches quando todos têm tabelas [MsiPatchSequence](msipatchsequence-table.md) , consulte o [exemplo de vários patches](multiple-patching-example.md).

 

 



