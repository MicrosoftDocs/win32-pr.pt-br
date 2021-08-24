---
description: Visão geral do DXVA 2 e sua relação com o DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Sobre o DXVA 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d6ab595be1f167f777e50001c8d31658dc697866c8d11db3865e66e87508ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606816"
---
# <a name="about-dxva-20"></a>Sobre o DXVA 2.0

A DXVA (Aceleração de Vídeo) do DirectX é uma API e um DDI correspondente para usar a aceleração de hardware para acelerar o processamento de vídeo. Codecs de software e processadores de vídeo de software podem usar o DXVA para descarregar determinadas operações com uso intensivo de CPU para a GPU. Por exemplo, um decodificador de software pode descarregar a iDCT (transformação cosseno discreta) inversa para a GPU.

No DXVA, algumas operações de decodificação são implementadas pelo driver de hardware de gráficos. Esse conjunto de funcionalidades é o *acelerador*. Outras operações de decodificação são implementadas pelo software de aplicativo no modo de usuário, chamado *de decodificador de host* ou *decodificador de software*. (Os termos *decodificador de* host e *decodificador de software* são equivalentes.) O processamento executado pelo acelerador é chamado de processamento fora *do host.* Normalmente, o acelerador usa a GPU para acelerar algumas operações. Sempre que o acelerador executa uma operação de decodificação, o decodificador de host deve transmitir para os buffers de acelerador que contêm as informações necessárias para executar a operação

A API DXVA 2 requer Windows Vista ou posterior. A API do DXVA 1 ainda é compatível com o Windows Vista para compatibilidade com compatibilidade com compatibilidade com backward. Uma camada de emulação é fornecida que é convertida entre qualquer versão da API e a versão oposta da DDI:

-   Se o driver gráfico estiver em conformidade com o WDDM (modelo de driver de exibição) do Windows, as chamadas à API DXVA 1 serão convertidas em chamadas DDI DXVA 2.
-   Se os drivers gráficos usarem o XPDM (modelo de driver de exibição) mais antigo do Windows XP, as chamadas à API DXVA 2 serão convertidas em chamadas DDI DXVA 1.

A tabela a seguir mostra os requisitos do sistema operacional e os renderadores de vídeo com suporte para cada versão da API DXVA.



| Versão da API | Requisitos          | Suporte ao renderador de vídeo                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 ou posterior | Sobreposição Mixer, VMR-7, VMR-9 (somente DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow e Media Foundation)         |



 

No DXVA 1, o decodificador de software deve acessar a API por meio do renderador de vídeo. Não é possível usar a API DXVA 1 sem chamar o renderador de vídeo. Essa limitação foi removida com o DXVA 2. Usando o DXVA 2, o decodificador de host (ou qualquer aplicativo) pode acessar a API diretamente, por meio da interface [**IDirectXVideoDecoderService.**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)

A documentação do DXVA 1 descreve as estruturas de decodificação usadas para os seguintes padrões de vídeo:

-   ITU-T Rec. H.261
-   ITU-T Rec. H.263
-   Vídeo do MPEG-1
-   Vídeo perfil principal do MPEG-2

As especificações a seguir definem extensões DXVA para outros padrões de vídeo:

-   [Especificação DXVA para decodificação H.264/AVC](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [Especificação DXVA para H.264/MPEG-4 MVC MVC (Multiview Video Coding), incluindo o perfil alto estéreo](https://www.microsoft.com/download/details.aspx?id=25200)
-   [Especificação DXVA para MPEG-1 VLD e Decodificação de vídeo MPEG-1/MPEG-2 combinada.](https://www.microsoft.com/download/details.aspx?id=9374)
-   [Especificação DXVA para Off-Host vld para decodificação de vídeo mpeg-4 parte 2](https://www.microsoft.com/download/details.aspx?id=21100)
-   [Especificação DXVA para Windows vídeo de mídia® v8, v9 e vA Decodificação (incluindo SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [Especificação DXVA (Aceleração de Vídeo) do DirectX para codificação de vídeo escalonável H.264/MPEG-4 (SVC) Off-Host modo VLD](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [Especificação de aceleração de vídeo do DirectX para codificação de vídeo VP8 e VP9](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 e DXVA 2 usam as mesmas estruturas de dados para decodificação. No entanto, o procedimento para configurar a sessão de decodificação foi alterado. O DXVA 1 usa um mecanismo de "investigação e bloqueio", no qual o decodificador de host pode testar várias configurações antes de definir a configuração desejada no acelerador. No DXVA 2, o acelerador retorna uma lista de configurações com suporte e o decodificador de host seleciona uma na lista. Os detalhes são dados nas seções a seguir:

-   [Suporte ao DXVA 2.0 no DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Suporte ao DXVA 2.0 no Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Especificação do DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
