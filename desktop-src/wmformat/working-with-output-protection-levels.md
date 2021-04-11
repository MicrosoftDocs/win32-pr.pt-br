---
title: Trabalhando com níveis de proteção de saída
description: Trabalhando com níveis de proteção de saída
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- SDK do Windows Media Format, níveis de proteção de saída (OPL)
- SDK do Windows Media Format, níveis de proteção
- ASF (Advanced Systems Format), níveis de proteção de saída (OPL)
- ASF (formato de sistemas avançados), níveis de proteção de saída (OPL)
- ASF (Advanced Systems Format), níveis de proteção
- ASF (formato de sistemas avançados), níveis de proteção
- ASF (Advanced Systems Format), várias licenças
- ASF (formato de sistemas avançados), várias licenças
- DRM (gerenciamento de direitos digitais), OPL (níveis de proteção de saída)
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
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293754"
---
# <a name="working-with-output-protection-levels"></a>Trabalhando com níveis de proteção de saída

As licenças criadas usando o SDK do Windows Media Rights Manager 10 podem especificar restrições de ação usando os níveis de proteção de saída (OPLs). OPLs habilite um criador de licença para permitir algumas ações somente em dispositivos com tecnologias específicas. Os benefícios de usar o OPLs é que você obtém mais flexibilidade na criação de restrições de licença do que as versões anteriores. Além disso, o OPLs é expansível para acomodar tecnologias futuras. Você pode dar suporte a tais licenças em seus aplicativos usando os métodos da interface [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .

Para ler os arquivos que são protegidos por uma licença que especifica OPLs, você deve verificar o OPL para a ação desejada. A tecnologia de saída que seu aplicativo está usando deve ser permitida pelo OPL na licença. Por exemplo, algumas licenças para áudio protegido podem exigir que você use o caminho de áudio seguro para reproduzi-lo.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configurando o leitor para avaliar os níveis de proteção de saída

Antes de poder verificar OPLs para arquivos carregados no leitor, você deve chamar o método [**IWMDRMReader2:: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , passando **true** para o parâmetro *fEvaluate* . Se você não chamar esse método, as licenças que exigem OPLs não serão visíveis para seu aplicativo.

## <a name="evaluating-copy-output-protection-levels"></a>Avaliando níveis de proteção de saída de cópia

Para obter os níveis de proteção de saída para a ação de cópia, chame o método [**IWMDRMReader2:: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) . Os dados recebidos da chamada são armazenados em uma estrutura [**OPL de \_ cópia \_ do DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) . A estrutura contém um nível de proteção de saída base, que especifica o nível de saída mínimo para a ação de cópia na licença. No entanto, \_ a \_ estrutura OPL de cópia do DRM também contém duas listas de identificadores de tecnologia: uma para tecnologias permitidas que são classificadas em um OPL mais baixo do que a base e outra para tecnologias que são classificadas de forma igual ou superior à OPL base, mas que são restritas pela licença. Você deve verificar as inclusões e exclusões para garantir que a tecnologia que seu aplicativo está usando seja permitida pela licença.

## <a name="evaluating-play-output-protection-levels"></a>Avaliando níveis de proteção de saída de reprodução

Para obter os níveis de proteção de saída para a ação de reprodução, chame o método [**IWMDRMReader2:: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) . Os dados recebidos da chamada são armazenados em uma estrutura [**OPL de \_ reprodução \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) . A estrutura contém várias outras estruturas. Os níveis de proteção de saída de base para a ação de reprodução são armazenados em uma estrutura de níveis de  [**\_ \_ \_ proteção \_ de saída mínima de DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (o membro minOPL do **DRM \_ Play \_ OPL**), que define o mínimo de OPL necessário para reproduzir conteúdo em uma variedade de formatos. Você deve verificar o membro para o tipo de formatos de saída que seu aplicativo fornece.

A **estrutura \_ \_ OPL de reprodução do DRM** define dois tipos de restrições: os identificadores de proteção de saída de vídeo permitidos e de amostragem necessários.

Requerido-a amostragem é definida como uma lista de identificadores de tecnologia de saída (o membro **oplIdDownsample** do **\_ \_ OPL de reprodução DRM**) que, se usado, pode receber o conteúdo para reprodução somente se o conteúdo estiver primeiro abaixo de amostra para uma taxa de bits inferior.

Os identificadores de proteção de saída de vídeo permitidos são definidos como uma lista de tecnologias de saída de vídeo com informações de configuração para cada uma.

## <a name="handling-multiple-licenses"></a>Lidando com várias licenças

Alguns arquivos podem ter várias licenças associadas a eles no repositório de licenças local. Ao avaliar OPLs para um arquivo que você está lendo, você pode verificar licenças adicionais chamando o método [**IWMDRMReader2:: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) . Você deve continuar tentando as licenças até encontrar uma que permita a ação que deseja executar ou até que TryNextLicense retorne o DRM \_ S \_ false, o que indica que não há mais licenças.

Em alguns casos, um arquivo pode ter uma licença associada que exige um OPL para o qual seu aplicativo não possa dar suporte. Nesse caso, é importante verificar licenças adicionais, pois pode haver uma licença que não especifique OPLs.

**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interface IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




