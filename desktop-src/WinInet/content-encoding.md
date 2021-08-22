---
title: Codificação de Conteúdo
description: A partir do Windows Server 2008 e Windows Vista, o aplicativo pode direcionar o WinINet para executar a decodificação de conteúdo para os esquemas de codificação de conteúdo gzip e deflate.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Codificação de Conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1a91120e4ea01c4636c8d9942e968a0d69aeed50b6a037b31aa0241f3e933c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132879"
---
# <a name="content-encoding"></a>Codificação de Conteúdo

Conforme especificado nos aplicativos de protocolo HTTP (RFC 2616) podem solicitar que o servidor retorne respostas HTTP no formato codificado. Antes do Windows Server 2008 e Windows Vista, as solicitações com codificação de conteúdo eram enviadas ao aplicativo para processamento em seu nível. A partir do Windows Server 2008 e Windows Vista, o aplicativo pode direcionar o WinINet para executar a decodificação de conteúdo para os esquemas de codificação de conteúdo gzip e deflate.

Para habilitar a decodificação de conteúdo, o aplicativo define a opção de decodificação solicitando que o WinINet execute a decodificação em seu nome. No entanto, a habilitação da decodificação não garante que o WinINet executará a decodificação de conteúdo e o aplicativo deve estar preparado para lidar com a decodificação. O WinINet retira o título de codificação de conteúdo da resposta quando a decodificação de conteúdo é executada com êxito. Espera-se que os aplicativos lidam com a decodificação de conteúdo, independentemente de a opção de decodificação estar habilitada ou desabilitada quando o header de codificação de conteúdo estiver presente na resposta.

Quando a decodificação é habilitada, o aplicativo deve especificar a lista de codificações com suporte no Accept-Encoding da solicitação. O Accept-Encoding, no entanto, não obligate o servidor para enviar uma resposta codificada. O WinINet enviará respostas que não corresponderão à lista de codificações aceitáveis de volta para o aplicativo.

A lista a seguir descreve as condições sob as quais o WinINet executará a decodificação de conteúdo quando a opção estiver habilitada:

-   O Accept-Encoding deve estar presente na solicitação e deve especificar os esquemas de codificação gzip, deflate ou gzip e deflate.
-   O esquema de codificação especificado no título Content-Encoding deve corresponder a um dos esquemas de codificação especificados no Accept-Encoding de dados.
-   O header Content-Encoding na resposta especifica apenas um esquema de codificação.
-   A resposta deve conter apenas um header Content-Encoding. O WinINet decodifica o conteúdo codificado com apenas um esquema de codificação.
-   O Cache-Control não deve conter a diretiva no-transform.
-   O header Content-Range não deve estar presente na resposta.

## <a name="setting-the-decompression-option"></a>Definindo a opção de descompactação

A opção de decodificação pode ser definida no alça de sessão, no alça de solicitação ou no alça de conexão. O handle no qual a opção de decodificação está definida define o escopo da opção de decodificação. Por exemplo, definir a decodificação na sessão habilita a decodificação de todas as conexões e solicitações criadas nesse lidar.

Para definir a opção de decodificação, o aplicativo chama [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) com o handle retornado de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). A **opção INTERNET OPTION HTTP \_ \_ \_ DECODING** é especificada no parâmetro *dwOption* e o parâmetro *lpBuffer* aponta para uma variável booliana definida como true. Para desabilitar a decodificação, o aplicativo chama **InternetSetOption com** a opção **INTERNET OPTION HTTP \_ \_ \_ DECODING** e a variável booliana definida como false.

Quando a opção de decodificação é definida, o WinINet executa a decodificação na solicitação quando o aplicativo chama [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Se o WinINet encontrar um erro ao executar a decodificação de conteúdo, a chamada para **InternetReadFile** falhará com um **ERRO \_ DECODIFICAÇÃO DA INTERNET \_ COM \_ FALHA.** Quando a decodificação falha, o aplicativo tem duas opções: ele pode remover o cabeçalho do Accept-Encoding e reendá-la ou pode definir a opção **\_ INTERNET OPTION HTTP \_ \_ DECODING** na solicitação como false e, em seguida, reendá-la. Se a opção de decodificação for definida como false, o aplicativo deverá verificar o header Content-Encoding e executar qualquer decodificação no nível do aplicativo.

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 