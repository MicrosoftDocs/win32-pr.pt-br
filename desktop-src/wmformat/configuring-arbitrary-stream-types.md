---
title: Configurando tipos de fluxo arbitrários
description: Configurando tipos de fluxo arbitrários
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- fluxos, configurando tipos de fluxo arbitrários
- codecs, configurando tipos de fluxo arbitrários
- fluxos, GenProfile
- codecs, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780363"
---
# <a name="configuring-arbitrary-stream-types"></a>Configurando tipos de fluxo arbitrários

A maioria dos tipos de fluxo arbitrários precisa apenas de uma taxa de bits, uma janela de buffer e um tipo de mídia principal adequado na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . No entanto, alguns tipos arbitrários exigem configuração adicional.

Se você tiver problemas para configurar um fluxo, consulte o aplicativo de exemplo chamado GenProfile, que está incluído neste SDK. A biblioteca definida em GenProfile contém código para incluir todos os tipos de fluxos. Para obter mais informações sobre GenProfile e outros exemplos, consulte [aplicativos de exemplo](sample-applications.md).

As seções a seguir descrevem como configurar tipos de fluxo arbitrários.



| Seção                                                                                                                                        | Descrição                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configurando fluxos de script](configuring-script-streams.md)                                                                                   | Descreve como configurar fluxos de script.                                                  |
| [Configurando fluxos de transferência de arquivo](configuring-file-transfer-streams.md)                                                                     | Descreve como configurar fluxos de transferência de arquivo.                                           |
| [Configurando fluxos da Web](configuring-web-streams.md)                                                                                         | Descreve como configurar fluxos da Web.                                                     |
| [Configurando fluxos de texto](configuring-text-streams.md)                                                                                       | Descreve como configurar fluxos de texto.                                                    |
| [Configurando fluxos arbitrários personalizados](configuring-custom-arbitrary-streams.md)                                                               | Descreve como configurar fluxos para tipos de fluxos arbitrários personalizados.                       |
| [Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Descreve como calcular a taxa de bits e as configurações de janela de buffer para um fluxo arbitrário. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos arbitrários**](arbitrary-streams.md)
</dt> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> </dl>

 

 




