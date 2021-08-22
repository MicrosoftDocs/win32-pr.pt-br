---
title: Backup em fita
description: Um volume de fita consiste em uma mídia de gravação e sua operadora física. Cada volume de fita tem uma ou mais partições. As partições normalmente são divididas em seções por marcas de arquivo ou setmarks. Há três tipos de marcas de arquivo.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- backup Backup , fita
- Backup de backup em fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217c1a536b8a1a345218d3748c6207e9b336b84eca4cea0f4e48b4e84c521733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588826"
---
# <a name="tape-backup"></a>Backup em fita

Um *volume de fita* consiste em uma mídia de gravação e sua operadora física. Todo o comprimento da fita em um volume não está disponível para gravação de dados. Seções curtas no início e no final da fita são reservadas para anexar a fita aos hubs na operadora. A primeira posição na fita em que os dados podem ser registrados é o chamado de marcador de início de médio *e* a última posição é chamada de marcador de fim *de médio.*

Cada volume de fita tem uma ou mais partições. Uma partição é uma parte do volume, que contém seus próprios pontos inicial e final, que não se sobrepõem a nenhuma outra parte do volume. Cada partição tem três posições predefinida. A primeira posição em uma partição em que você pode registrar dados é chamada de marcador de início da partição *e* a última é chamada de marcador de fim *de partição*. O *marcador de aviso antecipado* está localizado imediatamente antes do marcador de fim da partição. A posição de aviso antecipado notifica os aplicativos de fita para transferir dados armazenados em buffer para a fita antes de alcançar o marcador de fim da partição.

A área entre os pontos inicial e final de uma partição normalmente é dividida em seções por marcas *de* arquivo ou *setmarks*. Marcas de arquivo e marcas de definição são elementos gravados especiais que não contêm dados do usuário; eles simplesmente dividem a partição em áreas menores para fornecer um esquema de endereço. Marcas de arquivo e marcas de definição têm finalidades semelhantes, mas as marcas de definição fornecem um posicionamento mais rápido em unidades de fita de alta capacidade.

Normalmente, os dispositivos de fita são compatíveis com marcas de arquivo e setmarks. O suporte de ambos permite que os dados de fita sejam formatados de modo que setmarks separem dados de diferentes volumes de disco e marcas de arquivo separem dados de arquivos individuais em um volume de disco.

Outro elemento gravado que denota locais na fita é uma lacuna de apagaamento, uma área de fita apagada ou um padrão que o dispositivo não reconhece como uma marca ou como dados de usuário.

Há três tipos de marcas de arquivo. Uma *marca de arquivo curta* contém uma breve lacuna de apagaamento que não pode ser substituída, a menos que a operação de gravação seja executada desde o início da partição ou de uma marca de arquivo longa anterior. Uma *marca de arquivo* longa contém uma lacuna de apagação longa que permite que um aplicativo posicione a fita no início da marca de arquivo e sobrescreva a marca de arquivo e a lacuna de apagação. Uma *marca de arquivo normal* não contém uma lacuna de apagação. Os dispositivos de fita que usam marcas de arquivo são compatíveis com marcas de arquivo curtas e longas ou marcas de arquivo normais, mas não todas as três.

A área em uma partição entre marcas de arquivo ou marcas de arquivo está disponível para gravação de dados. Uma unidade de dados gravados ou lidos de uma fita é conhecida como um bloco.

Para obter mais informações, consulte estes tópicos:

-   [Inicialização de fita](tape-initialization.md)
-   [Entrada e saída de fita](tape-input-and-output.md)
-   [Criando um aplicativo de backup](creating-a-backup-application.md)
-   [Fazer o back-up e restaurar links rígidos](backing-up-and-restoring-hard-links.md)

 

 




