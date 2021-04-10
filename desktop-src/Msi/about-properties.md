---
description: Windows Installer pode configurar a instalação do software usando os valores das variáveis definidas em um pacote de instalação ou pelo usuário.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Sobre propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169222"
---
# <a name="about-properties"></a>Sobre propriedades

Windows Installer pode configurar a instalação do software usando os valores das variáveis definidas em um pacote de instalação ou pelo usuário.

Windows Installer usa três categorias de variáveis globais durante uma instalação:

-   Propriedades particulares: o instalador usa propriedades privadas internamente e seus valores devem ser criados no banco de dados de instalação ou definidos para valores determinados pelo ambiente operacional.
-   Propriedades públicas: as propriedades públicas podem ser criadas no banco de dados e alteradas por um usuário ou administrador do sistema na linha de comando, aplicando uma transformação ou interagindo com uma interface do usuário criada.
-   Propriedades públicas restritas: para fins de segurança, o autor de um pacote de instalação pode restringir as propriedades públicas que um usuário pode alterar.

Nem todas as propriedades precisam ser definidas em todos os pacotes, há um pequeno conjunto de propriedades necessárias que devem ser definidas em todos os pacotes. O instalador define os valores das propriedades em uma determinada ordem de precedência.

[Propriedades particulares](private-properties.md)

[Propriedades públicas](public-properties.md)

[Propriedades públicas restritas](restricted-public-properties.md)

[Propriedades obrigatórias](required-properties.md)

[Ordem de precedência de propriedade](order-of-property-precedence.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando propriedades](using-properties.md)
</dt> <dt>

[Referência de propriedade](property-reference.md)
</dt> </dl>

 

 



