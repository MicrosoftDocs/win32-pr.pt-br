---
title: Reutilizando configurações de fluxo
description: Reutilizando configurações de fluxo
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- fluxos, reutilizando configurações
- perfis, reutilizando configurações de fluxo
- Reutilizando configurações de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ee1a2b51d5a2a659cb24955ab74a5fb285308125b21781c9d42a709d7e4b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110186"
---
# <a name="reusing-stream-configurations"></a>Reutilizando configurações de fluxo

Geralmente, há ocasiões em que você deseja reutilizar um objeto de configuração de fluxo de um perfil existente. Você pode ter perfis antigos que precisam de atualização ou pode precisar de um fluxo idêntico a um em um perfil de sistema. É mais fácil reutilizar configurações de fluxo do que criar novas, e muitas vezes você pode alterar algumas configurações em uma configuração para atender às suas necessidades em vez de criar uma totalmente nova.

Lembre-se de que há limitações em como você pode alterar as configurações de fluxo. Se você alterar as configurações de forma errada, seu perfil poderá não aceitar o objeto de configuração de fluxo. As configurações de fluxo incorretas são frequentemente aceitas pelo perfil, mas fazem com que o objeto do gravador rejeite o perfil. Esteja atento às seguintes limitações e problemas ao usar e modificar as configurações de fluxo existentes.

-   Nunca altere o conteúdo de um arquivo. prx para alterar as configurações de fluxo. Quando os perfis são salvos em cadeias de caracteres XML e gravados em um arquivo. prx, eles podem ser lidos com qualquer editor de texto. Examinar um perfil salvo pode ajudá-lo a entender como os perfis funcionam. No entanto, você nunca deve alterar um arquivo. prx de forma alguma. Mesmo alterações aparentemente triviais podem invalidar o perfil.
-   várias versões do Windows codec de áudio de mídia usam as mesmas configurações de fluxo. se você tiver um objeto de configuração de fluxo configurado como subtipo WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAudioV7 ou WMMEDIASUBTYPE \_ WMAudioV8, o fluxo resultante será compactado com o codec de áudio de mídia mais recente Windows. No entanto, você deve avaliar suas necessidades antes de usar um codec de áudio existente. muitos tipos de arquivos podem ser aprimorados atualizando para a versão mais recente do codec Windows media audio Professional ou o codec de mídia sem perdas de áudio Windows.
-   Nunca altere o subtipo de um fluxo para atualizar para um novo codec. Quando você usa os métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para obter uma configuração de fluxo, o codec anexa alguns dados a ele que identifica o formato de fluxo de bits. Se você alterar o subtipo de um objeto de configuração de fluxo existente, o subtipo não corresponderá aos dados do codec. Um perfil com essa configuração de fluxo não será aceito pelo objeto do gravador.
-   Não altere as configurações de configurações de fluxo de áudio compactado. Se as configurações de um fluxo de áudio não atenderem às suas necessidades, obtenha uma nova configuração de fluxo do codec usando os métodos de **IWMCodecInfo3**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configurando Fluxos**](configuring-streams.md)
</dt> <dt>

[**Obtendo informações de configuração de fluxo de codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




