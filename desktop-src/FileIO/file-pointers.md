---
description: Um ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Ponteiros de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdfe744f341e111e7956bda85401c5b87e063718309f675c33ff551918756239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997027"
---
# <a name="file-pointers"></a>Ponteiros de arquivo

Quando um arquivo é aberto, Windows associa um ponteiro *de arquivo* ao fluxo padrão. Esse ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado. Sempre que um arquivo é aberto, o sistema coloca o ponteiro do arquivo no início do arquivo, que é o deslocamento zero. Cada operação de leitura e gravação avança o ponteiro do arquivo pelo número de bytes que estão sendo lidos e gravados. Por exemplo, se o ponteiro do arquivo estiver no início do arquivo e uma operação de leitura de 5 bytes for solicitada, o ponteiro do arquivo será localizado no deslocamento 5 imediatamente após a operação de leitura. À medida que cada byte é lido ou gravado, o sistema avança o ponteiro do arquivo. O ponteiro do arquivo também pode ser reposicionado chamando a [**função SetFilePointer.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)

Quando o ponteiro do arquivo atinge o final de um arquivo e o aplicativo tenta ler do arquivo, nenhum erro ocorre, mas nenhum bytes é lido. Portanto, ler zero bytes sem um erro significa que o aplicativo atingiu o final do arquivo. Escrever zero bytes não faz nada.

Um aplicativo pode truncar ou estender um arquivo usando a [**função SetEndOfFile.**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) Essa função define o final do arquivo para a posição atual do ponteiro de arquivo.

 

 



