---
description: A partir do Windows Server 2008 e Windows Vista, a API WinHTTP foi aprimorada para incluir os recursos a seguir.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Novidades no Windows Server 2008 e Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e474bbfa32d8f82737df4be6f537ca0a6f1bc870e2028d7dcdb1f418adb7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071696"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Novidades no Windows Server 2008 e Windows Vista

A partir do Windows Server 2008 e Windows Vista, a API WinHTTP foi aprimorada para incluir os recursos a seguir.

## <a name="greater-than-4-gb-upload"></a>Maior que 4 GB Upload.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) pode enviar apenas 4 GB de dados devido a limitações no tamanho do parâmetro de comprimento total DWORD. Para permitir que os aplicativos enviem mais de 4 GB de dados, o header Content-Length é adicionado à solicitação especificando dados tão grandes quanto um INTEIRO GRANDE \_ (2^64 bytes). Para obter mais informações, **consulte WinHttpSendRequest**. Não há suporte para esse recurso no [**objeto COM IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="transfer-encoding-header"></a>Transfer-Encoding de Transfer-Encoding

O Transfer-Encoding de dados permite que os aplicativos enviem dados em partes para o servidor. Quando o Transfer-Encoding está presente na solicitação, o aplicativo envia a solicitação com um corpo de entidade de comprimento zero na chamada para [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). O corpo da entidade é enviado em chamadas subsequentes para [**WinHttpWriteData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) Não há suporte para esse recurso no [**objeto COM IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Recuperação da lista de emissores de certificados do cliente SSL

O aplicativo pode recuperar a lista de emissores do certificado do cliente SSL quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) falhar com um **ERRO \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**. Uma nova opção, **WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ ISSUER \_ LIST,** permite que os aplicativos recuperem a Lista de Emissores do certificado e filtrem a lista para o certificado ideal. Para obter mais informações, consulte os [**tópicos Sinalizadores**](option-flags.md) de Opção e Recuperação de Lista de Emissores [para Autenticação de Cliente SSL.](ssl-in-winhttp.md) Não há suporte para esse recurso no [**objeto COM IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="optional-client-certificates"></a>Certificados de cliente opcionais

Quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) falha com um **ERRO \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**, o servidor pode não exigir o certificado do cliente SSL. O servidor pode ser capaz de reverter para outra forma de autenticação ou permitir que o cliente continue com acesso anônimo. O aplicativo define a **opção WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ CONTEXT** e especifica uma macro que o WinHttp usa para determinar se o certificado do cliente é necessário. Para obter mais informações, consulte [**Sinalizadores de opção**](option-flags.md). Não há suporte para esse recurso no [**objeto COM IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="source-and-destination-ip-addresses"></a>Endereços IP de origem e destino

Quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) for concluído, o aplicativo poderá recuperar o endereço IP de origem e de destino e a porta da solicitação que gerou a resposta. Uma nova estrutura é fornecida para receber os endereços de origem e de destino quando a **opção WINHTTP \_ OPTION CONNECTION \_ \_ INFO** é definida. Para obter mais informações, consulte [**Sinalizadores de opção**](option-flags.md). Não há suporte para esse recurso no [**objeto COM IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="additional-ssl-client-authentication-errors"></a>Erros adicionais de autenticação de cliente SSL

Erros adicionais de autenticação de cliente SSL fornecem mais informações sobre o certificado do cliente SSL. **ERRO \_ WINHTTP \_ CLIENT CERT NO PRIVATE \_ \_ \_ \_ KEY** and **ERROR \_ WINHTTP \_ CERT NO ACCESS PRIVATE KEY \_ \_ \_ \_ certificate** certificate errors are new for Windows Server 2008 and Windows Vista. O [**objeto COM IWinHttpRequest**](iwinhttprequest-interface.md) retorna esses erros em um HRESULT.

 

 



