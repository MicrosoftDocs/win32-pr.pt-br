---
title: Consistência de transferência de arquivo
description: O BITS garante que a versão do arquivo que ele transfere seja consistente com base no tamanho do arquivo e no carimbo de data/hora, não no conteúdo (o BITS não protege contra ataques man-in-the-middle).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608566f6e9927fdcb39133c30720a46ead869f36d3084c950b9ed86379c4b749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959495"
---
# <a name="file-transfer-consistency"></a>Consistência de transferência de arquivo

O BITS garante que a versão do arquivo que ele transfere seja consistente com base no tamanho do arquivo e no carimbo de data/hora, não no conteúdo (o BITS não protege contra ataques man-in-the-middle). Para verificar o conteúdo por conta própria, você pode usar o método [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) para obter o nome do arquivo que contém o conteúdo baixado, verificar o conteúdo usando seu próprio mecanismo e, em seguida, chamar o método [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) para indicar ao BITS se o conteúdo do arquivo é válido. Se você definir o estado de validação como **FALSE** e o conteúdo for do servidor de origem, o trabalho entrará no estado de erro. Se o conteúdo for de um par, o BITS baixará o arquivo do servidor de origem.

Para downloads, se o tamanho do arquivo ou o carimbo de data/hora mudar enquanto o BITS estiver transferindo o arquivo, o BITS reiniciará a transferência desse arquivo apenas. Por exemplo, se o trabalho de download contiver dois arquivos e os arquivos são atualizados no servidor enquanto o BITS estiver transferindo o segundo arquivo, o BITS reiniciará a transferência somente do segundo arquivo. O primeiro arquivo, que já foi transferido com êxito, não é atualizado para refletir as novas alterações.

Observe que, se você tiver o arquivo que está sendo baixado do servidor, deverá criar uma nova URL para cada nova versão do arquivo. Se você usar a mesma URL para novas versões do arquivo, alguns servidores proxy poderão servir dados desajustados do cache porque eles não verificam com o servidor original se o arquivo está desaloqueado.

Para uploads, se o tamanho do arquivo ou o carimbo de data/hora mudar durante a transferência de arquivo, o BITS gerará um erro e o trabalho será colocado no estado ERRO DE ESTADO DO TRABALHO \_ \_ \_ BG.

O BITS não sincroniza solicitações de transferência quando um ou mais usuários solicitam que o mesmo arquivo seja transferido para o mesmo local. O BITS transfere o arquivo para cada solicitação separadamente.

 

 




