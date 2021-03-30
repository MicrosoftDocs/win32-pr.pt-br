---
title: Protocolo de carregamento de BITS
description: Esta seção descreve o protocolo de rede para o upload de BITS e os tipos de trabalho de resposta de upload.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635116"
---
# <a name="bits-upload-protocol"></a>Protocolo de carregamento de BITS

Esta seção descreve o protocolo de rede para o upload de BITS e os tipos de trabalho de resposta de upload. O protocolo de carregamento BITS é colocado em camadas sobre HTTP 1,1 e usa muitos dos cabeçalhos HTTP existentes e define novos cabeçalhos. O protocolo de carregamento do BITS dá suporte a um único arquivo de carregamento por sessão.

O BITS usa pacotes para descrever solicitações de cliente e respostas do servidor. O cabeçalho BITS-pacote-tipo especifica o tipo de pacote que está sendo enviado. Cada pacote contém cabeçalhos específicos. O BITS usa o \_ verbo post do bits para identificar os pacotes de carregamento do bits. Os pacotes de resposta sempre usam o tipo de pacote ACK, que representa a confirmação. O pacote ACK é enviado no contexto da solicitação anterior; pode haver apenas uma solicitação pendente ao mesmo tempo.

Para trabalhos de resposta de upload, o BITS usa esse protocolo para carregar o arquivo, mas não usa esse protocolo para enviar a resposta ao cliente. Em vez disso, o servidor BITS envia o local do arquivo de resposta para o cliente e o cliente cria um trabalho de download do BITS para baixar o arquivo de resposta.

Use o protocolo de upload para substituir o cliente BITS ou o software de servidor pela sua própria implementação. Para obter uma lista de pacotes de solicitação enviados pelo cliente BITS, consulte [pacotes de solicitação do bits](bits-request-packets.md). Para obter uma lista de pacotes de resposta enviados pelo servidor BITS, consulte [pacotes de resposta do bits](bits-response-packets.md).

O cliente determina como ele responde a erros ou a pacotes inesperados do servidor BITS. Se o servidor receber um pacote que não espera, o servidor deverá enviar um pacote ACK com um código de retorno 400 (solicitação inválida).

 

 




