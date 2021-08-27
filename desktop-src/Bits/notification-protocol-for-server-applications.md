---
title: Protocolo de notificação para aplicativos de servidor
description: O BITS usa a propriedade BITSServerNotificationType para determinar como o BITS envia o conteúdo do arquivo de carregamento para o aplicativo de servidor.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54e859730acaa1456624e9fa5c2302bc36efd9d085daeecdf234aef8f74729c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004933"
---
# <a name="notification-protocol-for-server-applications"></a>Protocolo de notificação para aplicativos de servidor

O BITS usa a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) para determinar como o bits envia o conteúdo do arquivo de carregamento para o aplicativo de servidor. Se a propriedade BITSServerNotificationType for definida como 1, [o bits passará o local do arquivo de carregamento em um cabeçalho](#sending-the-location-of-the-upload-file-in-a-header). Se a propriedade BITSServerNotificationType for definida como 2, [o bits passará o conteúdo do arquivo de carregamento no corpo da solicitação](#sending-the-upload-file-in-the-body-of-the-request).

Para obter detalhes sobre como o BITS lida com erros do aplicativo de servidor, consulte [Manipulando erros de aplicativo do servidor](#handling-server-application-errors).

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>Enviando o local do arquivo de carregamento em um cabeçalho

O BITS passará o local dos arquivos de upload e de resposta para o aplicativo de servidor nos cabeçalhos, se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) estiver definida como 1. O aplicativo de servidor abre o arquivo de upload, processa os dados e, em seguida, gera o arquivo de resposta. Por padrão, o BITS remove os arquivos de upload e de resposta do servidor depois de receber a resposta do aplicativo de servidor. Para que o BITS Copie o arquivo de upload para o local especificado pelo nome do arquivo remoto no trabalho, inclua o cabeçalho BITS-Copy-file-to-Destination em sua resposta. Se você não incluir o cabeçalho e quiser salvar os arquivos de upload e de resposta, deverá copiar os arquivos de upload e de resposta em um novo local antes de responder. A tabela a seguir mostra os cabeçalhos de solicitação.



| Cabeçalho da solicitação              | Descrição                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| BITS-original-solicitação-URL   | Contém o nome remoto especificado no trabalho.                                             |
| BITS-Request-DataFile-Name  | Contém o caminho completo para os dados carregados.                                               |
| BITS-Response-DataFile-Name | Contém o caminho completo para onde o BITS espera que o aplicativo de servidor grave a resposta. |



 

A tabela a seguir mostra os cabeçalhos de resposta.



| Cabeçalho de resposta               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-estático-resposta-URL      | Opcional. Contém a URL absoluta (não especifique uma URL relativa) para um arquivo de dados estático a ser usado como resposta. O arquivo de dados estáticos deve ser acessível pelo cliente BITS. Se você usar esse cabeçalho, não crie o arquivo de resposta especificado no cabeçalho de solicitação BITS-Response-DataFile-Name. Observe que o BITS não exclui esse arquivo para você.<br/>                                                                                                           |
| BITS-Copiar-arquivo-para-destino | Opcional. Por padrão, se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) for definida como 1 ou 2, o servidor bits não copiará o arquivo de carregamento para o local especificado pelo nome do arquivo remoto no trabalho. Para que o BITS Copie o arquivo para o local especificado pelo nome do arquivo remoto no trabalho, envie este cabeçalho de resposta. Você pode especificar qualquer valor; O BITS não usa o valor. Observe que as pastas no caminho do arquivo remoto devem existir. |



 

A solicitação a seguir mostra o BITS enviando o local do arquivo de carregamento para o aplicativo de servidor.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

O seguinte mostra a resposta do aplicativo do servidor para o BITS; a resposta é colocada no arquivo especificado pelo cabeçalho de solicitação BITS-Response-DataFile-Name.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>Enviando o arquivo de carregamento no corpo da solicitação

O BITS enviará o arquivo de carregamento no corpo da solicitação se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) estiver definida como 2. O envio do arquivo de upload no corpo da solicitação permite que os scripts e aplicativos existentes funcionem com modificações mínimas. O arquivo de upload e o arquivo de resposta são passados na solicitação e na resposta, respectivamente. A tabela a seguir mostra o cabeçalho da solicitação.



| Cabeçalho da solicitação            | Descrição                                    |
|---------------------------|------------------------------------------------|
| BITS-original-solicitação-URL | Contém o nome remoto especificado no trabalho. |



 

A tabela a seguir mostra os cabeçalhos de resposta.



| Cabeçalho de resposta               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-estático-resposta-URL      | Opcional. Contém a URL absoluta (não especifique uma URL relativa) para um arquivo de dados estático a ser usado como resposta. O arquivo de dados estáticos deve ser acessível pelo cliente BITS. Se você usar esse cabeçalho, não inclua a resposta no fluxo. Observe que o BITS não exclui esse arquivo para você.<br/>                                                                                                                                      |
| BITS-Copiar-arquivo-para-destino | Opcional. Se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) for definida como 1 ou 2, o servidor bits não copiará o arquivo de carregamento para o local especificado pelo nome do arquivo remoto no trabalho. Para que o BITS Copie o arquivo para o local especificado pelo nome do arquivo remoto, envie este cabeçalho de resposta. Você pode especificar qualquer valor; O BITS não usa o valor. Observe que as pastas no caminho do arquivo remoto devem existir. |



 

A solicitação a seguir mostra o BITS que transmite o arquivo carregado para o aplicativo de servidor no corpo da solicitação.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

A resposta a seguir mostra o aplicativo de servidor que passa os dados de resposta para BITS no corpo da resposta.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>Manipulando erros de aplicativo do servidor

Consulte [tratamento de erros de aplicativo do servidor](handling-server-application-errors.md).

 

 





