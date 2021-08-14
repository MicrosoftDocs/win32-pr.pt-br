---
title: Trabalhando com listas de revogação
description: Trabalhando com listas de revogação
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows SDK do formato de mídia, listas de revogação
- ASF (Advanced Systems Format), listas de revogação
- ASF (formato de sistemas avançados), listas de revogação
- listas de revogação
- DRM (gerenciamento de direitos digitais), listas de revogação
- DRM (gerenciamento de direitos digitais), listas de revogação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d022b9b55a1a14b147d76d289efeac956bae8f1858d155f138efa579d533fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194863"
---
# <a name="working-with-revocation-lists"></a>Trabalhando com listas de revogação

Para responder a violações de segurança e para garantir que os aplicativos do Player conhecidos como rompidos ou comprometidos não possam reproduzir ou usar arquivos protegidos, cada licença emitida conterá uma lista de revogação. Uma lista de revogação contém os certificados de aplicativo de todos os aplicativos do Player conhecidos como danificados ou corrompidos. Quando uma nova licença é recebida, o componente DRM do aplicativo de Player verifica se há uma lista de revogação. Se for encontrado um que seja mais recente do que o atualmente no computador, a lista mais recente será armazenada. Na próxima vez que o consumidor reproduzir um arquivo ASF protegido, o componente DRM compara o aplicativo de Player com a lista de revogação. Se o aplicativo de player for revogado, o componente DRM enviará uma mensagem de erro ao aplicativo.

Os aplicativos do Player podem receber uma mensagem de erro de revogação nos seguintes cenários:

-   A mensagem de erro é recebida depois que o aplicativo chama o método [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) para um arquivo protegido. A chamada falha com o código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revogado, que é fornecido para a função de retorno de chamada **OnStatus** com o \_ status de licença de aquisição WMT \_ . Se esse código **HRESULT** for ignorado, os erros continuarão ocorrendo.
-   A mensagem de erro é recebida quando o aplicativo cria o leitor habilitado para DRM e chama o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) para um arquivo protegido. A chamada falha com o código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revogado, que é fornecido para o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) com o \_ status aberto WMT. Quando um aplicativo de Player recebe essa mensagem de erro, o aplicativo deve notificar os usuários finais e fornecer uma maneira para que eles restaurem a funcionalidade para o Player. Por exemplo, o aplicativo pode abrir uma URL onde os usuários finais podem baixar uma atualização para o aplicativo comprometido.

**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Lidando com eventos de aquisição de licença**](handling-license-acquisition-events.md)
</dt> </dl>

 

 




