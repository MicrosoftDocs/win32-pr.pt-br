---
description: Agrupando aplicativos em partições
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Agrupando aplicativos em partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40491e95313544a32e23db78d8959736665db8c21782d3f1b30729e6eda6f1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991096"
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
| Um aplicativo de biblioteca<br/>   | Somente público. Caso contrário, o aplicativo chamador pode ter os mesmos componentes, o que criaria ambiguidade.<br/> |
| Na partição global<br/> | Somente público. Isso garante a compatibilidade com compatibilidade com backward.<br/>                                                             |



 

## <a name="application-ids"></a>IDs do aplicativo

Cada aplicativo COM+ instalado em um computador tem uma ID de aplicativo exclusiva. No entanto, os nomes de aplicativo só precisam ser exclusivos em uma única partição e não em todo o computador.

A tabela a seguir mostra o que acontece com a ID do aplicativo quando um aplicativo é importado para uma partição ou exportado de uma partição.



| Se um aplicativo for:                                              | Em seguida, a ID do aplicativo:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importado para a partição global<br/>                        | Permanece o mesmo<br/>                 |
| Importado para uma partição diferente da partição global<br/> | Foi alterado<br/>                       |
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

[Definindo direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




