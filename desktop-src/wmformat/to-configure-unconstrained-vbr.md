---
title: Para configurar a VBR não restringida
description: Para configurar a VBR não restringida
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, configurando a VBR não restringida
- taxa de bits variável (VBR), configurando irrestrito
- VBR (taxa de bits variável), configurando irrestrito
- perfis, configurando a VBR não restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084393"
---
# <a name="to-configure-unconstrained-vbr"></a>Para configurar a VBR não restringida

Você pode usar a codificação de taxa de bits variável (VBR) irrestrita em um fluxo para especificar uma taxa média de bits que será mantida no conteúdo codificado. A VBR não restringida difere da CBR normal, pois a variação em taxa de bits em todo o fluxo pode ser maior.

A taxa de bits do fluxo, definida com [**IWMStreamConfig::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)setaverage, é usada como a taxa de bits média desejada. Quando a codificação do fluxo estiver concluída, você poderá usar [**IWMPropertyVault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) para recuperar duas propriedades adicionais: **g \_ wszVBRPeak** e **g \_ wszBufferAverage**. Essas propriedades descrevem a taxa de bits de pico do conteúdo codificado e a janela de buffer médio do conteúdo, respectivamente.

A VBR não restringida deve ser usada em conjunto com codificação de duas passagens. A codificação de duas passagens não está definida no perfil. Você deve configurar o gravador para executar uma passagem de pré-processamento antes de gravar o fluxo. Para obter mais informações sobre como usar a codificação de duas passagens, consulte [usando a codificação Two-Pass](using-two-pass-encoding.md).

Para configurar um fluxo em um perfil a ser codificado com uma VBR não restringida, execute as seguintes etapas:

1.  Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Abra um perfil existente ao qual você deseja adicionar suporte a VBR. Para obter mais informações sobre como abrir perfis, consulte [trabalhando com perfis](working-with-profiles.md).
3.  Obtenha um objeto de configuração de fluxo para o fluxo que você deseja usar chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenha um ponteiro para a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.
5.  Habilite a codificação de VBR para o fluxo chamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para a propriedade **g \_ wszVBREnabled** .
6.  Defina **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** para zero com **IWMPropertyVault:: SetProperty**.
7.  Salve as alterações feitas no fluxo chamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Salve o perfil ou passe-o para o objeto gravador.
9.  Configure o gravador para executar uma passagem de pré-processamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos de VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




