---
title: Plug-ins do Windows Media Player
description: Plug-ins do Windows Media Player
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Windows Media Player, plug-ins
- Plug-ins do Windows Media Player, sobre
- plug-ins, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105785198"
---
# <a name="windows-media-player-plug-ins"></a>Plug-ins do Windows Media Player

O Microsoft Windows Media Player expõe interfaces que permitem estender a funcionalidade de várias maneiras. As seções a seguir descrevem as arquiteturas de plug-ins com suporte e o processo de criação de um plug-in:



| Seção                                                                                                         | Descrição                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criando um plug-in](building-a-plug-in.md)                                                                    | Você pode criar vários tipos de plug-ins usando o Visual Studio e o assistente de plug-in do Windows Media Player.                                                                                                                                                                                             |
| [Visualizações personalizadas do Windows Media Player](windows-media-player-custom-visualizations.md)                    | As visualizações do Windows Media Player são objetos Component Object Model (COM) usados para exibir imagens visuais que são sincronizadas com a parte de áudio da reprodução de mídia do Player. As visualizações personalizadas podem ser criadas usando Microsoft Visual C++.                                             |
| [Plug-ins de interface do usuário do Windows Media Player](windows-media-player-user-interface-plug-ins.md)                | Os plug-ins de interface de usuário do Windows Media Player adicionam nova funcionalidade ao painel em **execução** do player de modo completo. Você pode criar plug-ins que usam a área de visualização, uma janela separada, a área de configurações, a área de metadados ou plug-ins de segundo plano que não expõem nenhuma interface de usuário visível. |
| [Plug-ins de DSP do Windows Media Player](windows-media-player-dsp-plug-ins.md)                                      | Os plug-ins do DSP do Windows Media Player modificam ou processam dados de áudio e vídeo antes de serem renderizados pelo Player. Plug-ins do DSP são objetos de mídia do DirectX (DMO) que se conectam ao Player por meio de interfaces COM.                                                                                           |
| [Plug-ins de renderização do Windows Media Player (preterido)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85)) | Decodificação de plug-ins de renderização do Windows Media Player (se necessário) e renderização de dados personalizados contidos em um fluxo de formato de mídia do Windows. Os plug-ins de renderização são os objetos de mídia do DirectX (DMO) que se conectam ao Player por meio de interfaces COM.                                                                  |
| [Plug-ins de conversão do Windows Media Player](windows-media-player-conversion-plug-ins.md)                        | Os plug-ins de conversão do Windows Media Player convertem arquivos de mídia digital criados usando tecnologias não fornecidas pela Microsoft no formato ASF (Advanced Systems Format).                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**SDK do Windows Media Player**](windows-media-player-sdk.md)
</dt> </dl>

 

 