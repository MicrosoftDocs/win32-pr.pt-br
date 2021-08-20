---
description: Partições padrão
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Partições padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968f5daa811202f80ae8d916142c8182b684006720068841ac5f9ae86123f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102379"
---
# <a name="default-partitions"></a>Partições padrão

Quando uma partição padrão é atribuída a um usuário, o COM+ tenta ativar os componentes nessa partição primeiro. Se a ativação falhar, o COM+ pesquisará a partição global do componente a ser ativado. A exceção a esse processo ocorre quando o componente COM+ inclui um moniker de partição, que especifica explicitamente a partição na qual o componente está localizado. Nesse caso, o moniker da partição tem precedência sobre qualquer configuração de partição padrão.

Ao usar partições locais, a partição padrão é atribuída aos usuários usando a pasta **usuários da partição com+** na ferramenta administrativa serviços de componentes no servidor de aplicativos. Ao usar conjuntos de partições no Active Directory, a partição padrão do usuário é determinada pelo conjunto de partições do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Partições locais](local-partitions.md)
</dt> <dt>

[Propriedades da partição](partition-properties.md)
</dt> <dt>

[Partições e Active Directory](partitions-and-active-directory.md)
</dt> <dt>

[A partição global](the-global-partition.md)
</dt> </dl>

 

 



