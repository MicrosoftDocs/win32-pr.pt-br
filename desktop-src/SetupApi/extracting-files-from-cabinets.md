---
description: Você pode extrair arquivos de um gabinete de duas maneiras. A primeira e mais simples maneira é aproveitar o processamento automático de gabinete integrado às funções de instalação.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraindo arquivos de gabinetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfd7f41d4951e43bb58fac6efb9b1fd11895373398643e7c8c9cc00821dd72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887247"
---
# <a name="extracting-files-from-cabinets"></a>Extraindo arquivos de gabinetes

Você pode extrair arquivos de um gabinete de duas maneiras. A primeira e mais simples maneira é aproveitar o processamento automático de gabinete integrado às funções de instalação.

As funções de instalação, como [**SetupCommitFileQueue,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)e [**SetupInstallFromInfSection,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)verificam a compactação em cada arquivo. Se o arquivo estiver em um gabinete, as funções primeiro procurarão um arquivo com esse nome fora do gabinete. Se encontrado, as funções instalam o arquivo externo, ignorando o arquivo dentro do gabinete. Isso permite que você atualize um único arquivo dentro do gabinete sem recriar o gabinete.

As funções de instalação também rastreia quais arquivos em um gabinete foram recuperados, para que um arquivo seja extraído apenas uma vez, mesmo que ele seja instalado várias vezes.

A segunda maneira de extrair arquivos de um gabinete é usando [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Essa função itera em cada arquivo em um gabinete, enviando uma notificação para uma rotina de retorno de chamada para cada arquivo encontrado. A rotina de retorno de chamada retorna um valor que indica se o arquivo deve ser extraído ou ignorado.

> [!Note]  
> A API de Instalação não fornece uma rotina de retorno de chamada padrão para lidar com notificações de gabinete. Se você chamar [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitamente, deverá fornecer uma rotina de retorno de chamada para processar as notificações de gabinete retornadas pela função.

 

 

 



