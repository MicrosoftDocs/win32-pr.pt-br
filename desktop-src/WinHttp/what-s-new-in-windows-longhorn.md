---
description: A partir do Windows Server 2008 e do Windows Vista, a API do WinHTTP foi aprimorada para incluir os recursos a seguir.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: O que há de novo no Windows Server 2008 e no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0f274b45e1db79fb79340b7f490de96f57e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461128"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>O que há de novo no Windows Server 2008 e no Windows Vista

A partir do Windows Server 2008 e do Windows Vista, a API do WinHTTP foi aprimorada para incluir os recursos a seguir.

## <a name="greater-than-4-gb-upload"></a>Mais de 4 GB de upload.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) pode enviar apenas 4 GB de dados devido a limitações no tamanho do parâmetro de comprimento total DWORD. Para permitir que os aplicativos enviem mais de 4 GB de dados, o cabeçalho Content-Length é adicionado à solicitação especificando dados tão grandes quanto um \_ inteiro grande (2 ^ 64 bytes). Para obter mais informações, consulte **WinHttpSendRequest**. Não há suporte para esse recurso no objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="transfer-encoding-header"></a>Cabeçalho de Transfer-Encoding

O cabeçalho Transfer-Encoding permite que os aplicativos enviem dados em partes para o servidor. Quando o cabeçalho de Transfer-Encoding está presente na solicitação, o aplicativo envia a solicitação com um corpo de entidade de comprimento zero na chamada para [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). O corpo da entidade é enviado em chamadas subsequentes para [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata). Não há suporte para esse recurso no objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Recuperação da lista de emissores do certificado do cliente SSL

O aplicativo pode recuperar a lista de emissores de certificado de cliente SSL quando o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) falhar com um **erro de certificado de autenticação de \_ \_ cliente WinHTTP \_ \_ \_ necessário**. Uma nova opção, **a \_ \_ lista de \_ \_ emissor \_ de certificado de cliente de opção WinHTTP**, permite que os aplicativos recuperem a lista de emissores de certificado e filtrem a lista para o certificado ideal. Para obter mais informações, consulte os tópicos [**sinalizadores de opção**](option-flags.md) e [recuperação da lista de emissor para autenticação de cliente SSL](ssl-in-winhttp.md) . Não há suporte para esse recurso no objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="optional-client-certificates"></a>Certificados de cliente opcionais

Quando o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) falha com um erro de certificado de **autenticação de \_ cliente WinHTTP \_ \_ \_ \_ necessário**, o servidor pode não exigir o certificado de cliente SSL. O servidor pode ser capaz de reverter para outra forma de autenticação ou permitir que o cliente prossiga com o acesso anônimo. O aplicativo define a opção de **contexto de certificado de \_ cliente da opção \_ \_ \_ WinHTTP** e especifica uma macro que o WinHTTP usa para determinar se o certificado do cliente é necessário. Para obter mais informações, consulte [**sinalizadores de opção**](option-flags.md). Não há suporte para esse recurso no objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="source-and-destination-ip-addresses"></a>Endereços IP de origem e de destino

Quando o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) é concluído, o aplicativo pode recuperar o endereço IP de origem e de destino e a porta da solicitação que gerou a resposta. Uma nova estrutura é fornecida para receber os endereços de origem e de destino quando a opção de **\_ informações de \_ conexão \_ da opção WinHTTP** está definida. Para obter mais informações, consulte [**sinalizadores de opção**](option-flags.md). Não há suporte para esse recurso no objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="additional-ssl-client-authentication-errors"></a>Erros de autenticação de cliente SSL adicionais

Erros adicionais de autenticação de cliente SSL fornecem mais informações sobre o certificado de cliente SSL. **Erro \_ do O certificado do \_ cliente WinHTTP \_ não é \_ uma \_ \_ chave privada** e o **erro \_ WinHTTP \_ CERT \_ no \_ Access \_ \_ chave privada não acesso** erros de certificado de cliente são novos para o Windows Server 2008 e o Windows Vista. O objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) retorna esses erros em um HRESULT.

 

 



