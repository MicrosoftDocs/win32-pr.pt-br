---
title: Manipulando eventos de individualização
description: Manipulando eventos de individualização
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows SDK de Formato de Mídia, manipulando eventos de individualização
- Windows SDK de Formato de Mídia, eventos de individualização
- ASF (Advanced Systems Format), manipulando eventos de individualização
- ASF (Formato de Sistemas Avançados), manipulando eventos de individualização
- FORMATO DE SISTEMAS Avançados (ASF), eventos de individualização
- ASF (Formato de Sistemas Avançados), eventos de individualização
- DRM (gerenciamento de direitos digitais), manipulando eventos de individualização
- DRM (gerenciamento de direitos digitais), manipulando eventos de individualização
- DRM (gerenciamento de direitos digitais), eventos de individualização
- DRM (gerenciamento de direitos digitais), eventos de individualização
- eventos de individualização
- eventos, eventos de individualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895710558c58fca108915ad1a73a0354c1fb39feb662fa3e2c698dadbe4cbe76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433606"
---
# <a name="handling-individualization-events"></a>Manipulando eventos de individualização

Quando um aplicativo habilitado para DRM tenta abrir um arquivo protegido, o componente DRM examina o atributo [**\_ DRM DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) no arquivo, que especifica o nível mínimo de versão necessário para acessar o conteúdo. Todos os níveis do componente DRM funcionam com todas as versões 7.0 e posteriores do Windows Media Player e o SDK Windows Formato de Mídia. Se o nível de versão individualizado do componente DRM for inferior à versão necessária, o componente DRM enviará um evento **WMT \_ NEEDS \_ INDIVIDUALIZATION** para o método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do aplicativo. Em seguida, o aplicativo deve exibir uma mensagem ou caixa de diálogo solicitando que os usuários iniciem ou cancelem a atualização de segurança. Esse prompt é necessário porque, por motivos de privacidade, os usuários devem dar suas permissões antes que uma atualização de segurança seja instalada em seu computador.

> [!Note]  
> O título do conteúdo especifica apenas os dois primeiros dígitos para \_ DRM DRMVersion \_ IndividualizedVersion. Em outras palavras, para exigir um componente DRM de nível 2.2.0.1, o header conteria "2.2".

 

Para iniciar a atualização de segurança e/ou disparar a individualização, chame o método [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) com o parâmetro *dwFlags* definido como 1.

Você deve manipular o **evento WMT \_ INDIVIDUALIZE** em seu aplicativo. Esse evento será acionado várias vezes pelo componente DRM com o status do processo de individualização indicado no parâmetro *pValue,* que é lançado em um ponteiro para uma estrutura [**WM \_ INDIVIDUALIZE \_ STATUS.**](wm-individualize-status.md)

Depois que o componente DRM for individualizado com êxito, o aplicativo receberá um evento **WMT \_ NO RIGHTS \_ \_ EX,** indicando que o aplicativo agora pode prosseguir para adquirir uma licença para o conteúdo.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos de aquisição de licença**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualizando aplicativos DRM**](individualizing-drm-applications.md)
</dt> <dt>

[**IWMDRMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




