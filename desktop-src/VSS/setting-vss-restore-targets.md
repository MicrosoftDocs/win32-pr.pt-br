---
description: A interface IVssComponent permite que um gravador ajuste exatamente como os arquivos são restaurados em uma base componente por componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Definindo destinos de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797488"
---
# <a name="setting-vss-restore-targets"></a>Definindo destinos de restauração do VSS

A interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite que um gravador ajuste exatamente como os arquivos são restaurados em uma base componente por componente.

Como é possível que a configuração do sistema durante a restauração seja algo diferente daquele previsto durante o backup, o mecanismo de destino de restauração é fornecido.

Ele permite que os gravadores chamem [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) para alterar a forma como os componentes [*incluídos explicitamente*](vssgloss-e.md) no documento de componentes de backup são restaurados. Isso também altera o mecanismo de restauração usado nesses componentes que são [*incluídos implicitamente*](vssgloss-i.md).

Restauração de arquivo que ocorre durante uma reinicialização do sistema (sob os valores de enumeração de enumeração do [**VSS \_ \_ RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) o VSS \_ RME \_ Restore \_ na \_ reinicialização e o VSS \_ RME \_ Restore \_ na \_ reinicialização \_ se \_ não puder \_ substituir) não pode ser afetado por destinos de restauração porque não há serviços VSS em execução quando **MoveFileEx** copia arquivos para o local final.

Da mesma forma, as \_ \_ restaurações personalizadas do VSS RME podem ou não ser afetadas, porque cada restauração personalizada é específica para um determinado gravador e pode optar por respeitar ou ignorar destinos de restauração.

Os solicitantes e gravadores podem usar [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) para verificar o destino de restauração de um conjunto de componentes.

O [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) dá suporte aos seguintes destinos de restauração, que podem ser definidos em um conjunto de componentes pela base do conjunto de componentes:

-   ORIGINAL do VSS \_ RT \_ . O método de restauração especificado pela enumeração de [**\_ \_ Enumeração RESTOREMETHOD do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) será respeitado.
-   alternativa do VSS \_ RT \_ . Os arquivos são restaurados em um local determinado a partir de um mapeamento de local alternativo existente. Se houver um mapeamento de local alternativo correspondente a um caminho em um subcomponente do conjunto de componentes, restaure para o local alternativo, se possível; caso contrário, retorne um erro.

 

 



