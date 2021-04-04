---
title: Para configurar a VBR restrita
description: Para configurar a VBR restrita
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, configurando a taxa de bits restrita
- taxa de bits variável (VBR), configurando a restrição
- VBR (taxa de bits variável), configurando a restrição
- perfis, configurando a VBR restrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007236"
---
# <a name="to-configure-constrained-vbr"></a>Para configurar a VBR restrita

Você pode usar a codificação de taxa de bits variável restrita (VBR) em um fluxo para especificar uma taxa média de bits que será mantida no conteúdo codificado. Você também especifica a taxa de bits máxima do fluxo e a janela de buffer máxima necessária.

Você não pode saber qual será a taxa de bits média para um fluxo de VBR restrita antes da codificação, mas você pode usar uma estimativa aproximada. Como regra geral, a taxa de bits máxima especificada acabará sendo de duas a três vezes a taxa média de bits.

A taxa de bits restrita deve ser usada em conjunto com codificação de duas passagens. A codificação de duas passagens não está definida no perfil. Você deve configurar o gravador para executar uma passagem de pré-processamento antes de gravar o fluxo. Para obter mais informações sobre como usar a codificação de duas passagens, consulte [usando a codificação Two-Pass](using-two-pass-encoding.md).

Para configurar um fluxo em um perfil para usar a codificação de VBR restrita, execute as etapas a seguir.

1.  Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Abra um perfil existente ao qual você deseja adicionar suporte a VBR. Para obter mais informações sobre como abrir perfis, consulte [trabalhando com perfis](working-with-profiles.md).
3.  Obtenha um objeto de configuração de fluxo para o fluxo que você deseja usar chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenha um ponteiro para a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.
5.  Habilite a codificação de VBR para o fluxo chamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para a propriedade **g \_ wszVBREnabled** .
6.  Use chamadas para **IWMPropertyVault:: SetProperty** para definir os valores máximos desejados para as propriedades **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** .
7.  Salve as alterações feitas no fluxo chamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Salve o perfil ou passe-o para o objeto gravador.
9.  Configure o gravador para executar uma passagem de pré-processamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos de VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




