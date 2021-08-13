---
title: Trabalhando com níveis de proteção de saída
description: Trabalhando com níveis de proteção de saída
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows SDK de Formato de Mídia, níveis de proteção de saída (OPL)
- Windows SDK de Formato de Mídia, níveis de proteção
- ASF (Advanced Systems Format), níveis de proteção de saída (OPL)
- ASF (Formato de Sistemas Avançados), níveis de proteção de saída (OPL)
- ASF (Advanced Systems Format), níveis de proteção
- ASF (Formato de Sistemas Avançados), níveis de proteção
- ASF (Advanced Systems Format), várias licenças
- ASF (Formato de Sistemas Avançados), várias licenças
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), níveis de proteção
- DRM (gerenciamento de direitos digitais), níveis de proteção
- DRM (gerenciamento de direitos digitais), avaliando os níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), avaliando os níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), várias licenças
- DRM (gerenciamento de direitos digitais), várias licenças
- níveis de proteção de saída (OPL)
- OPL (níveis de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2888891e50ec90e784bf6f4420637544854a9b600b5538e9655bc6d3028f76d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697710"
---
# <a name="working-with-output-protection-levels"></a>Trabalhando com níveis de proteção de saída

As licenças criadas usando o SDK Windows Media Rights Manager 10 podem especificar restrições de ação usando OPLs (níveis de proteção de saída). As OPLs permitem que um criador de licenças permita algumas ações somente em dispositivos com tecnologias específicas. Os benefícios de usar OPLs é que você tem mais flexibilidade na criação de restrições de licença do que as versões anteriores. Além disso, as OPLs são expansíveis para acomodar tecnologias futuras. Você pode dar suporte a essas licenças em seus aplicativos usando os métodos da interface [**IWMDRMReader2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)

Para ler arquivos protegidos por uma licença que especifica OPLs, você deve verificar o OPL para a ação desejada. A tecnologia de saída que seu aplicativo está usando deve ser permitida pelo OPL na licença. Por exemplo, algumas licenças para áudio protegido podem exigir que você use o caminho de áudio seguro para reproduzi-lo.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configurando o leitor para avaliar níveis de proteção de saída

Antes de verificar as OPLs para arquivos carregados no leitor, você deve chamar o método [**IWMDRMReader2::SetEvaluateOutputLevelLicenses,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) passando **TRUE** para o parâmetro *fEvaluate.* Se você não chamar esse método, as licenças que exigem OPLs não serão visíveis para seu aplicativo.

## <a name="evaluating-copy-output-protection-levels"></a>Avaliando níveis de proteção de saída de cópia

Para obter níveis de proteção de saída para a ação de cópia, chame o [**método IWMDRMReader2::GetCopyOutputLevels.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) Os dados recebidos da chamada são armazenados em uma estrutura [**\_ \_ OPL COPY do DRM.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) A estrutura contém um nível de proteção de saída base, que especifica o nível mínimo de saída para a ação de cópia na licença. No entanto, a estrutura OPL COPY do DRM também contém duas listas de identificadores de tecnologia: uma para tecnologias permitidas que são classificadas em um OPL inferior à base e outra para tecnologias classificadas como iguais ou maiores que o OPL base, mas que são restritas pela \_ \_ licença. Você deve verificar as inclusões e exclusões para garantir que a tecnologia que seu aplicativo está usando seja permitida pela licença.

## <a name="evaluating-play-output-protection-levels"></a>Avaliando níveis de proteção de saída de reprodução

Para obter níveis de proteção de saída para a ação de reprodução, chame o [**método IWMDRMReader2::GetPlayOutputLevels.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) Os dados recebidos da chamada são armazenados em uma estrutura [**\_ \_ OPL DO DRM PLAY.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) A estrutura contém várias outras estruturas. Os níveis de proteção de saída base para a ação de reprodução são armazenados em uma estrutura [**DRM \_ MINIMUM OUTPUT PROTECTION \_ \_ \_ LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (o membro **minOPL** do **DRM PLAY \_ \_ OPL**), que define o OPL mínimo necessário para reproduzir conteúdo em uma variedade de formatos. Você deve verificar o membro quanto ao tipo de formatos de saída que seu aplicativo fornece.

A **estrutura \_ \_ OPL DO DRM PLAY** define dois tipos de restrições: a amostragem inomeada necessária e identificadores de proteção de saída de vídeo permitidos.

A amostragem inocesa necessária é definida como uma lista de identificadores de tecnologia de saída (o **membro oplIdDownsample** do **DRM \_ PLAY \_ OPL**) que, se usado, poderá receber o conteúdo para reprodução somente se o conteúdo for primeiro amostrado para uma taxa de bits menor.

Os identificadores de proteção de saída de vídeo permitidos são definidos como uma lista de tecnologias de saída de vídeo com informações de configuração para cada um.

## <a name="handling-multiple-licenses"></a>Manipulando várias licenças

Alguns arquivos podem ter várias licenças associadas a eles no armazenamento de licenças local. Ao avaliar as OPLs de um arquivo que está lendo, você pode verificar se há licenças adicionais chamando o método [**IWMDRMReader2::TryNextLicense.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) Você deve continuar tentando licenças até encontrar uma que permita a ação que deseja executar ou até que TryNextLicense retorne DRM S FALSE, o que indica que não há mais \_ \_ licenças.

Em alguns casos, um arquivo pode ter uma licença associada que requer um OPL que seu aplicativo não possa dar suporte. Nesse caso, é importante verificar se há licenças adicionais porque pode existir uma licença que não especifique OPLs.

**Observação** O DRM não é suportado pela versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




