---
description: Você pode extrair arquivos de um gabinete de duas maneiras. A primeira e mais simples é aproveitar o processamento automático de gabinetes incorporados às funções de instalação.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraindo arquivos de gabinetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750426"
---
# <a name="extracting-files-from-cabinets"></a>Extraindo arquivos de gabinetes

Você pode extrair arquivos de um gabinete de duas maneiras. A primeira e mais simples é aproveitar o processamento automático de gabinetes incorporados às funções de instalação.

As funções de instalação, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), verificam a compactação em cada arquivo. Se o arquivo estiver em um gabinete, as funções primeiro pesquisarão um arquivo com esse nome fora do gabinete. Se for encontrado, as funções instalarão o arquivo externo, ignorando o arquivo dentro do gabinete. Isso permite que você atualize um único arquivo dentro do gabinete sem recriar o gabinete.

As funções de instalação também controlam quais arquivos em um gabinete foram recuperados, para que um arquivo seja extraído apenas uma vez, mesmo que ele seja instalado várias vezes.

A segunda maneira de extrair arquivos de um gabinete é usando [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Essa função itera em cada arquivo em um gabinete, enviando uma notificação para uma rotina de retorno de chamada para cada arquivo encontrado. A rotina de retorno de chamada retorna um valor que indica se o arquivo deve ser extraído ou ignorado.

> [!Note]  
> A API de instalação não fornece uma rotina de retorno de chamada padrão para manipular notificações de gabinete. Se você chamar [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitamente, deverá fornecer uma rotina de retorno de chamada para processar as notificações de gabinete que a função retorna.

 

 

 



