---
title: Manipulando eventos de individualização
description: Manipulando eventos de individualização
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows SDK de formato de mídia, tratando eventos de individualização
- Windows SDK do formato de mídia, eventos de individualização
- ASF (Advanced Systems Format), tratando eventos de individualização
- ASF (formato de sistemas avançados), tratando eventos de individualização
- ASF (Advanced Systems Format), eventos de individualização
- ASF (formato de sistemas avançados), eventos de individualização
- DRM (gerenciamento de direitos digitais), tratando eventos de individualização
- DRM (gerenciamento de direitos digitais), manipulação de eventos de individualização
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

Quando um aplicativo habilitado para DRM tenta abrir um arquivo protegido, o componente DRM examina o atributo [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) no arquivo, que especifica o nível mínimo de versão necessário para acessar o conteúdo. todos os níveis do componente DRM funcionam com todas as versões 7,0 e posteriores do Windows Media Player e o SDK do formato de mídia do Windows. Se o nível de versão individual do componente DRM for menor do que a versão necessária, o componente DRM enviará um evento de **\_ \_ individualização de WMT precisará** para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do aplicativo. O aplicativo deve exibir uma mensagem ou caixa de diálogo solicitando que os usuários iniciem ou cancelem a atualização de segurança. Esse prompt é necessário porque, por motivos de privacidade, os usuários devem conceder sua permissão antes que uma atualização de segurança seja instalada em seu computador.

> [!Note]  
> O cabeçalho do conteúdo especifica apenas os dois primeiros dígitos para DRM \_ DRMVersion \_ IndividualizedVersion. Em outras palavras, para exigir um componente 2.2.0.1 DRM de nível, o cabeçalho conterá "2,2".

 

Para iniciar a atualização de segurança e/ou disparar a individualização, chame o método [**IWMDRMReader:: individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) com o parâmetro *dwFlags* definido como 1.

Você deve manipular o **evento \_ individual WMT** em seu aplicativo. Esse evento será acionado várias vezes pelo componente DRM com o status do processo de individualização indicado *no parâmetro atingir* , que é convertido em um ponteiro para uma estrutura de [**\_ \_ status individual do WM**](wm-individualize-status.md) .

Depois que o componente DRM for individualizado com êxito, o aplicativo receberá um evento **WMT \_ no \_ Rights \_ ex** , indicando que o aplicativo agora pode continuar a adquirir uma licença para o conteúdo.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lidando com eventos de aquisição de licença**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualizando aplicativos DRM**](individualizing-drm-applications.md)
</dt> <dt>

[**Interface IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




