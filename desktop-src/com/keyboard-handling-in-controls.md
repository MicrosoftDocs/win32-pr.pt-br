---
title: Manipulação de teclado em controles
description: Manipulação de teclado em controles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811600"
---
# <a name="keyboard-handling-in-controls"></a>Manipulação de teclado em controles

O suporte ao manuseio de teclado para a funcionalidade a seguir é altamente recomendável, embora seja reconhecido que ele não seja aplicável a todos os contêineres.

-   Suporte para \_ bits de status OLEMISC ACTSLIKELABEL e OLEMISC \_ ACTSLIKEBUTTON.
-   Implementando a propriedade de ambiente DisplayAsDefault (se existir, ela pode retornar **false**).
-   Implementando a manipulação de guias, incluindo a ordem de tabulação.

Alguns contêineres usarão controles ActiveX em cenários tradicionais de documento composto. Por exemplo, uma planilha pode permitir que um usuário insira um controle ActiveX em uma planilha. Nesses cenários, o contêiner faria o manuseio do teclado de forma diferente, pois a interface do teclado deve permanecer consistente com as expectativas do usuário de uma planilha. A documentação para esses produtos deve informar os usuários sobre as diferenças na manipulação de controle nesses diferentes cenários. Outros contêineres devem se esforçar para honrar a funcionalidade acima, incluindo a manipulação de mnemônico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 




