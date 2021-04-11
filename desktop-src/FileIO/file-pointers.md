---
description: Um ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Ponteiros de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165257"
---
# <a name="file-pointers"></a>Ponteiros de arquivo

Quando um arquivo é aberto, o Windows associa um *ponteiro de arquivo* ao fluxo padrão. Esse ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado. Cada vez que um arquivo é aberto, o sistema coloca o ponteiro do arquivo no início do arquivo, que é o deslocamento zero. Cada operação de leitura e gravação avança o ponteiro do arquivo pelo número de bytes que estão sendo lidos e gravados. Por exemplo, se o ponteiro do arquivo estiver no início do arquivo e uma operação de leitura de 5 bytes for solicitada, o ponteiro do arquivo estará localizado no deslocamento 5 imediatamente após a operação de leitura. À medida que cada byte é lido ou gravado, o sistema avança o ponteiro do arquivo. O ponteiro do arquivo também pode ser reposicionado chamando a função [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .

Quando o ponteiro do arquivo atingir o final de um arquivo e o aplicativo tentar ler o arquivo, nenhum erro ocorrerá, mas nenhum byte será lido. Portanto, a leitura de zero bytes sem um erro significa que o aplicativo atingiu o final do arquivo. Escrever zero bytes não faz nada.

Um aplicativo pode truncar ou estender um arquivo usando a função [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) . Essa função define o fim do arquivo para a posição atual do ponteiro do arquivo.

 

 



