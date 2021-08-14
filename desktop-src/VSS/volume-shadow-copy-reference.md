---
description: O Serviço de Cópias de Sombra de Volume (VSS) é um conjunto de APIs COM e C++ que permite que os backups de volume sejam executados enquanto os aplicativos no sistema (chamados gravadores) continuam a gravar nos volumes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Referência da API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbc2d0bec6d68572a67a1dc80327fb80028d7f8d98487f24fec24e2c2e65f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751523"
---
# <a name="volume-shadow-copy-api-reference"></a>Referência da API de cópia de sombra de volume

O Serviço de Cópias de Sombra de Volume (VSS) é um conjunto de APIs COM e C++ que permite que os backups de volume sejam executados enquanto os aplicativos no sistema (chamados gravadores) continuam a gravar nos volumes.

O VSS dá suporte a esses backups por meio da criação de cópias de sombra, uma duplicata do volume original em um determinado momento.

Desenvolvedores de terceiros podem usar a API do VSS para criar solicitantes (como um aplicativo de backup) para criar e gerenciar cópias de sombra.

O trabalho real de criar e representar cópias de sombra é conduzido por aplicativos de nível de sistema conhecidos como provedores.

Os desenvolvedores também podem usar a API para construir gravadores: aplicativos com reconhecimento de VSS capazes de coordenar operações de e/s com a criação e manipulação de cópias de sombra.

-   [Classes de API de cópia de sombra de volume](volume-shadow-copy-api-classes.md)
-   [Tipos de dados da API de cópia de sombra de volume](volume-shadow-copy-api-data-types.md)
-   [Enumerações de API de cópia de sombra de volume](volume-shadow-copy-api-enumeration-types.md)
-   [Funções da API de cópia de sombra de volume](volume-shadow-copy-api-functions.md)
-   [Interfaces de API de cópia de sombra de volume](volume-shadow-copy-api-interfaces.md)
-   [Estruturas de API de cópia de sombra de volume](volume-shadow-copy-api-structures.md)
-   [Glossário de cópia de sombra de volume](volume-shadow-copy-glossary.md)

Para obter mais informações sobre como escrever solicitantes e gravadores, consulte [usando o serviço de cópias de sombra de volume](using-the-volume-shadow-copy-service.md).

 

 



