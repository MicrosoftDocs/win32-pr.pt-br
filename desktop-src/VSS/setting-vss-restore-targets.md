---
description: A interface IVssComponent permite que um autor ajuste exatamente como os arquivos são restaurados em uma base componente por componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Definindo destinos de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9378fe8175970a8ccacb196414f3afafbcd583ad74f9aca438a3e9b6cf6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394186"
---
# <a name="setting-vss-restore-targets"></a>Definindo destinos de restauração do VSS

A interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite que um autor ajuste exatamente como os arquivos são restaurados em uma base componente por componente.

Como é possível que a configuração do sistema durante a restauração seja algo diferente do previsto durante o backup, o mecanismo de destino de restauração é fornecido.

Ele permite que os autores chamem [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) [](vssgloss-e.md) para alterar como os componentes incluídos explicitamente no Documento de Componentes de Backup são restaurados. Isso também altera o mecanismo de restauração usado nesses componentes que são [*incluídos implicitamente.*](vssgloss-i.md)

A restauração de arquivo que ocorre durante uma reinicialização do sistema (nos valores de enumeração [**VSS \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS RME RESTORE AT REBOOT e \_ \_ \_ \_ VSS \_ RME RESTORE AT REBOOT IF CANNOT REPLACE) não \_ \_ \_ \_ \_ \_  pode ser afetada pelos destinos de restauração porque não há serviços VSS em execução quando MoveFileEx copia arquivos para seu local final.

Da mesma forma, as restaurações PERSONALIZADAs do VSS RME podem ou não ser afetadas, pois cada restauração personalizada é específica a um determinado autor e pode optar por respeitar ou ignorar os \_ \_ destinos de restauração.

Solicitantes e autores podem usar [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) para verificar o destino de restauração de um conjunto de componentes.

[**O IVssComponent dá**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) suporte aos seguintes destinos de restauração, que podem ser definidos em um conjunto de componentes por conjunto de componentes:

-   VSS \_ RT \_ ORIGINAL. O método de restauração especificado pela enumeração [**\_ \_ ENUM RESTOREMETHOD do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) será respeitado.
-   VSS \_ RT \_ ALTERNATE. Os arquivos são restaurados para um local determinado de um mapeamento de local alternativo existente. Se houver um mapeamento de local alternativo que corresponde a um caminho em um subcomponente do conjunto de componentes, restaure para o local alternativo, se possível; caso contrário, retorne um erro.

 

 



