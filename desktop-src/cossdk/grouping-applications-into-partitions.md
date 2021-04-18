---
description: Agrupando aplicativos em partições
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Agrupando aplicativos em partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778518"
---
# <a name="grouping-applications-into-partitions"></a>Agrupando aplicativos em partições

Ao decidir como agrupar aplicativos em partições, os administradores precisam estar cientes de determinadas regras e restrições, incluindo as seguintes:

-   Um aplicativo pode ser instalado em uma ou mais partições.
-   Somente uma instância de um determinado componente pode existir em um aplicativo.

## <a name="public-and-private-components"></a>Componentes públicos e privados

Existem outras restrições ao decidir como agrupar aplicativos COM+. Essas restrições pertencem a componentes públicos versus privados em um aplicativo. Os componentes do aplicativo geralmente podem ser públicos ou privados. No entanto, ao agrupar aplicativos em partições, os administradores devem estar cientes de algumas restrições em relação a componentes públicos e privados. A tabela a seguir lista essas restrições.



| Se um aplicativo for:              | Em seguida, os componentes em uma partição podem ser:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Um aplicativo de servidor<br/>    | Público e privado.<br/>                                                                                           |
| Um aplicativo de biblioteca<br/>   | Somente público. Caso contrário, o aplicativo de chamadores poderia ter os mesmos componentes, o que criaria ambiguidade.<br/> |
| Na partição global<br/> | Somente público. Isso garante a compatibilidade com versões anteriores.<br/>                                                             |



 

## <a name="application-ids"></a>IDs de aplicativo

Cada aplicativo COM+ instalado em um computador tem uma ID de aplicativo exclusiva. No entanto, os nomes de aplicativos só precisam ser exclusivos em uma única partição e não em todo o computador.

A tabela a seguir mostra o que acontece com a ID do aplicativo quando um aplicativo é importado para uma partição ou exportada de uma partição.



| Se um aplicativo for:                                              | Em seguida, a ID do aplicativo:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importado para a partição global<br/>                        | Permanece o mesmo<br/>                 |
| Importado para uma partição que não seja a partição global<br/> | É alterado<br/>                       |
| Exportado<br/>                                                | Está incluído no arquivo exportado<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletando métricas de partição](collecting-partition-metrics.md)
</dt> <dt>

[Configurando o cache de partição](configuring-the-partition-cache.md)
</dt> <dt>

[Gerenciando partições locais](managing-local-partitions.md)
</dt> <dt>

[Gerenciando partições no Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Configurando direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




