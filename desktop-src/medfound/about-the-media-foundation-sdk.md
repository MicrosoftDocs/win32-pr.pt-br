---
description: Microsoft Media Foundation é a próxima geração de plataforma multimídia para Windows que permite que desenvolvedores, consumidores e provedores de conteúdo adotem a nova onda de conteúdo premium com robustez avançada, qualidade incomparável e interoperabilidade direta.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Sobre o Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782734"
---
# <a name="about-media-foundation"></a>Sobre o Media Foundation

Microsoft Media Foundation é a próxima geração de plataforma multimídia para Windows que permite que desenvolvedores, consumidores e provedores de conteúdo adotem a nova onda de conteúdo premium com robustez avançada, qualidade incomparável e interoperabilidade direta.

Media Foundation requer o Windows Vista ou posterior. Ele usa o COM (modelo de objeto de componente) e requer C/C++. A Microsoft não fornece uma API gerenciada para Media Foundation.

As APIs de Media Foundation fazem parte do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Para desenvolver um aplicativo Media Foundation, instale a versão mais recente do SDK do Windows.

## <a name="audio-and-video-quality"></a>Qualidade de áudio e vídeo

O Media Foundation foi projetado para atender aos desafios apresentados pelo conteúdo de alta definição. Os aprimoramentos de qualidade de áudio e vídeo feitos em toda a plataforma agora possibilitam a entrega de uma ótima experiência para o conteúdo de alta definição da próxima geração.

-   A DXVA (DirectX Video Acceleration) 2,0 oferece aceleração de vídeo mais eficiente, em comparação com a DXVA 1,0, com decodificação de vídeo mais robusta e simplificada e uso estendido de hardware no processamento de vídeo. Com o DXVA 2,0, o Windows pode lidar com alguns dos mais exigentes conteúdo de alta definição com alta qualidade e maior resiliência de problemas.

-   As informações de espaço de cores são preservadas em todo o pipeline de vídeo. Os usuários podem desfrutar do conteúdo de vídeo com fidelidade total. As informações de cor e as imagens entrelaçadas agora são passadas para o hardware para composições de passagem única. Preservar as informações de espaço de cores também reduz as conversões desnecessárias de espaço de cores, o que libera mais ciclos para processar conteúdo HD exigente.
-   O EVR (processador de vídeo avançado) oferece melhor suporte a tempo, processamento de vídeo aprimorado e maior resiliência de problemas. O suporte à reprodução de tela inteira foi aprimorado e a divisão de vídeo no modo de janela foi minimizada.
-   O Media Foundation usa o serviço do Agendador de classes de multimídia (MMCSS), um novo serviço do sistema no Windows Vista. O MMCSS permite que os aplicativos multimídia garantam que seu processamento de tempo-diferenciado recebe acesso priorizado aos recursos da CPU.

## <a name="content-access"></a>Acesso ao conteúdo

À medida que o entretenimento digital passa para a era de alta definição e o conteúdo se torna mais portátil e onipresente, a proteção de conteúdo se tornará parte integrante dos produtos de mídia digital. A extensibilidade do Media Foundation garante que ele possa dar suporte a essas tendências.

Além disso, Media Foundation extensibilidade permite que diferentes sistemas de proteção de conteúdo operem juntos.

## <a name="about-media-foundation"></a>Sobre o Media Foundation

Esta seção contém informações gerais sobre as APIs de Media Foundation. Informações detalhadas de programação podem ser encontradas no [Guia de programação de Media Foundation](media-foundation-programming-guide.md).



| Seção                                                                              | Descrição                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [O que há de novo para Media Foundation](whats-new-for-media-foundation.md)                | Descreve os novos recursos do Media Foundation.                               |
| [Cabeçalhos e bibliotecas do Media Foundation](media-foundation-headers-and-libraries.md) | Lista os arquivos de cabeçalho e biblioteca que definem as APIs de Media Foundation. |
| [Ferramentas de Media Foundation](media-foundation-tools.md)                                 | Descreve as ferramentas de desenvolvimento que estão disponíveis para Media Foundation.  |



 

O Media Foundation não está incluído nas edições N e KN do Windows 8. Para obter mais informações, consulte [Microsoft Windows Media Feature Pack para versões N e kN de todas as edições do Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



