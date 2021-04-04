---
title: Codificação de Conteúdo
description: A partir do Windows Server 2008 e do Windows Vista, o aplicativo pode direcionar o WinINet a executar a decodificação de conteúdo para os esquemas de codificação de conteúdo gzip e deflate.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Codificação de Conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b089ae2aa4cbacdfc9b6ebefe5cbdfc1bfc10e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008032"
---
# <a name="content-encoding"></a>Codificação de Conteúdo

Conforme especificado nos aplicativos do protocolo HTTP (RFC 2616), é possível solicitar que o servidor retorne respostas HTTP no formato codificado. Antes do Windows Server 2008 e do Windows Vista, as solicitações com codificação de conteúdo foram enviadas para o aplicativo para processamento em seu nível. A partir do Windows Server 2008 e do Windows Vista, o aplicativo pode direcionar o WinINet a executar a decodificação de conteúdo para os esquemas de codificação de conteúdo gzip e deflate.

Para habilitar a decodificação de conteúdo, o aplicativo define a opção de decodificação solicitando que o WinINet execute a decodificação em seu nome. No entanto, habilitar a decodificação não garante que o WinINet executará a decodificação de conteúdo e que o aplicativo deve estar preparado para lidar com a decodificação. O WinINet retira o cabeçalho de codificação de conteúdo da resposta quando a decodificação de conteúdo é executada com êxito. Espera-se que os aplicativos manipulem a decodificação de conteúdo independentemente de a opção de decodificação estar habilitada ou desabilitada quando o cabeçalho de codificação de conteúdo estiver presente na resposta.

Quando a decodificação está habilitada, o aplicativo deve especificar a lista de codificações com suporte no cabeçalho Accept-Encoding da solicitação. No entanto, o cabeçalho Accept-Encoding não obriga o servidor a enviar uma resposta codificada. O WinINet enviará respostas que não correspondam à lista de codificações aceitáveis de volta para o aplicativo.

A lista a seguir descreve as condições sob as quais o WinINet executará a decodificação de conteúdo quando a opção estiver habilitada:

-   O cabeçalho de Accept-Encoding deve estar presente na solicitação e deve especificar os esquemas de codificação gzip, deflate ou gzip e deflate.
-   O esquema de codificação especificado no cabeçalho de codificação de conteúdo deve corresponder a um dos esquemas de codificação especificados no cabeçalho de Accept-Encoding.
-   O cabeçalho Content-Encoding na resposta especifica apenas um esquema de codificação.
-   A resposta deve conter apenas um cabeçalho de codificação de conteúdo. O WinINet decodifica o conteúdo codificado com apenas um esquema de codificação.
-   O cabeçalho de Cache-Control não deve conter a diretiva no-Transform.
-   O cabeçalho de intervalo de conteúdo não deve estar presente na resposta.

## <a name="setting-the-decompression-option"></a>Configurando a opção de descompactação

A opção de decodificação pode ser definida no identificador de sessão, no identificador de solicitação ou no identificador de conexão. O identificador no qual a opção de decodificação é definida define o escopo da opção de decodificação. Por exemplo, definir a decodificação na sessão permitirá a decodificação de todas as conexões e solicitações criadas sob esse identificador.

Para definir a opção de decodificação, o aplicativo chama o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) com o identificador retornado de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). A opção **Internet \_ Option \_ http \_ decodificação** é especificada no parâmetro *dwOption* e o parâmetro *lpBuffer* aponta para uma variável booleana definida como true. Para desabilitar a decodificação, o aplicativo chama o **InternetSetOption** com a opção **Internet \_ Option \_ http \_ decodificação** e a variável booliana definida como false.

Quando a opção de decodificação é definida, o WinINet executa a decodificação na solicitação quando o aplicativo chama [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Se o WinINet encontrar um erro ao executar a decodificação de conteúdo, a chamada para **InternetReadFile** falhará com um **erro de \_ decodificação de Internet com \_ \_ falha**. Quando a decodificação falha, o aplicativo tem duas opções: ele pode remover o cabeçalho Accept-Encoding e reenviar a solicitação, ou pode definir a opção **Internet \_ Option \_ http \_ decodificação** na solicitação como false e, em seguida, reenviar a solicitação. Se a opção de decodificação for definida como false, o aplicativo deverá verificar o cabeçalho de codificação de conteúdo e executar qualquer decodificação no nível do aplicativo.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 