---
title: Consistência de transferência de arquivo
description: O BITS garante que a versão do arquivo que ele transfere seja consistente com base no tamanho do arquivo e no carimbo de data/hora, não conteúdo (o BITS não protege contra ataques man-in-the-Middle).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822298"
---
# <a name="file-transfer-consistency"></a>Consistência de transferência de arquivo

O BITS garante que a versão do arquivo que ele transfere seja consistente com base no tamanho do arquivo e no carimbo de data/hora, não conteúdo (o BITS não protege contra ataques man-in-the-Middle). Para verificar o conteúdo por conta própria, você pode usar o método [**IBackgroundCopyFile3:: Gettemporárioname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) para obter o nome do arquivo que contém o conteúdo baixado, verificar o conteúdo usando seu próprio mecanismo e, em seguida, chamar o método [**IBackgroundCopyFile3:: setvalidable**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) para indicar ao bits se o conteúdo do arquivo for válido. Se você definir o estado de validação como **false** e o conteúdo for do servidor de origem, o trabalho entrará no estado de erro. Se o conteúdo for de um par, o BITS baixará o arquivo do servidor de origem.

Para downloads, se o tamanho do arquivo ou o carimbo de data/hora for alterado enquanto o BITS estiver transferindo o arquivo, o BITS reiniciará a transferência somente desse arquivo. Por exemplo, se o trabalho de download contiver dois arquivos e os arquivos forem atualizados no servidor enquanto o BITS estiver transferindo o segundo arquivo, o BITS reiniciará a transferência somente do segundo arquivo. O primeiro arquivo, que já foi transferido com êxito, não é atualizado para refletir as novas alterações.

Observe que, se você possuir o arquivo que está sendo baixado do servidor, deverá criar uma nova URL para cada nova versão do arquivo. Se você usar a mesma URL para novas versões do arquivo, alguns servidores proxy poderão atender a dados obsoletos de seu cache porque eles não verificam com o servidor original se o arquivo está obsoleto.

Para carregamentos, se o tamanho do arquivo ou o carimbo de data/hora for alterado durante a transferência de arquivo, o BITS gerará um erro e o trabalho será colocado no estado de erro BG do \_ estado do trabalho \_ \_ .

O BITS não sincroniza solicitações de transferência quando um ou mais usuários solicitam que o mesmo arquivo seja transferido para o mesmo local. O BITS transfere o arquivo para cada solicitação separadamente.

 

 




