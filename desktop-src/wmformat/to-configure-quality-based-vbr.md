---
title: Para configurar Quality-Based VBR
description: Para configurar Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, configurando a taxa de bits baseada em qualidade
- taxa de bits variável (VBR), configurando com base na qualidade
- VBR (taxa de bits variável), configurando com base na qualidade
- perfis, configurando a taxa de bits baseada em qualidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b1181d722909478b29e1ffbe5f5b53cb919d80e3922e055eecdf34c334a382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845630"
---
# <a name="to-configure-quality-based-vbr"></a>Para configurar Quality-Based VBR

Você pode usar a codificação de taxa de bits variável (VBR) com base em qualidade em um fluxo para especificar um nível de qualidade que será mantido para todo o fluxo, independentemente dos requisitos de taxa de bits resultantes.

Para fluxos de vídeo de taxa de bits VBR com base na qualidade, você deve especificar um nível de qualidade de 1 a 100, com 100 representando a qualidade mais alta. No momento, há apenas 30 configurações de qualidade discretas. Os níveis de qualidade a seguir correspondem a configurações de qualidade discretas: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. Os números entre dois valores consecutivos na lista anterior equivalem à mesma configuração de qualidade que o número mais baixo. Por exemplo, 1 e 4 são listados, portanto 2 e 3 resultam na mesma configuração de qualidade que 1.

Para fluxos de áudio, você pode enumerar os modos disponíveis e recuperar um objeto de configuração de fluxo. Para obter mais informações, consulte [para enumerar formatos de codec](to-enumerate-codec-formats.md).

Ao usar o vídeo VBR com base na qualidade, você deve definir o membro **dwBitrate** da estrutura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) para um valor positivo. Esse valor não é usado pelo gravador, mas passar zero ou um número negativo pode causar erros durante a gravação.

Para configurar um fluxo em um perfil a ser codificado com a VBR com base em qualidade, execute as etapas a seguir.

1.  Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Abra um perfil existente ao qual você deseja adicionar suporte a VBR. Para obter mais informações sobre como abrir perfis, consulte [trabalhando com perfis](working-with-profiles.md).
3.  Obtenha um objeto de configuração de fluxo para o fluxo que você deseja usar chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenha um ponteiro para a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.
5.  Habilite a VBR para o fluxo chamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para a propriedade **g \_ wszVBREnabled** .
6.  Defina o nível de qualidade para o fluxo de VBR chamando **IWMPropertyVault:: SetProperty** para a propriedade **g \_ wszVBRQuality** .
7.  Defina **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** para zero com **IWMPropertyVault:: SetProperty**.
8.  Salve as alterações feitas no fluxo chamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
9.  Salve o perfil ou passe-o para o objeto gravador e comece a escrever.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configurando Fluxos de VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




