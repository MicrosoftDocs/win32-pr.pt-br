---
description: Visão geral do DXVA 2 e sua relação com o DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Sobre o DXVA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751604"
---
# <a name="about-dxva-20"></a>Sobre o DXVA 2,0

A DXVA (aceleração de vídeo do DirectX) é uma API e uma DDI correspondente para usar a aceleração de hardware para acelerar o processamento de vídeo. Os codecs de software e os processadores de vídeo de software podem usar o DXVA para descarregar determinadas operações com uso intensivo de CPU para a GPU. Por exemplo, um decodificador de software pode descarregar a transformação de cosseno discreto inverso (iDCT) para a GPU.

No DXVA, algumas operações de decodificação são implementadas pelo driver de hardware de gráficos. Esse conjunto de funcionalidades é chamado de *acelerador*. Outras operações de decodificação são implementadas pelo software de aplicativo no modo de usuário, chamado de *decodificador de host* ou *decodificador de software*. (Os termos decodificador de *host* e *decodificador de software* são equivalentes.) O processamento executado pelo acelerador é chamado de *processamento fora do host*. Normalmente, o acelerador usa a GPU para acelerar algumas operações. Sempre que o acelerador executa uma operação de decodificação, o decodificador do host deve transmitir para os buffers do acelerador que contêm as informações necessárias para executar a operação

A API DXVA 2 requer o Windows Vista ou posterior. A API DXVA 1 ainda tem suporte no Windows Vista para compatibilidade com versões anteriores. Uma camada de emulação é fornecida que converte entre qualquer versão da API e a versão oposta da DDI:

-   Se o driver de gráficos estiver em conformidade com o WDDM (Windows Display Driver Model), as chamadas de API de DXVA 1 serão convertidas em chamadas de DDI de DXVA 2.
-   Se os drivers gráficos usarem o modelo de driver de vídeo do Windows XP mais antigo (XPDM), as chamadas à API de DXVA 2 serão convertidas em chamadas de DDI de DXVA 1.

A tabela a seguir mostra os requisitos do sistema operacional e os processadores de vídeo com suporte para cada versão da API de DXVA.



| Versão da API | Requisitos          | Suporte ao processador de vídeo                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 ou posterior | Mixer de sobreposição, VMR-7, VMR-9 (somente DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow e Media Foundation)         |



 

No DXVA 1, o decodificador de software deve acessar a API por meio do processador de vídeo. Não é possível usar a API DXVA 1 sem chamar o processador de vídeo. Essa limitação foi removida com o DXVA 2. Usando o DXVA 2, o decodificador de host (ou qualquer aplicativo) pode acessar a API diretamente, por meio da interface [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .

A documentação do DXVA 1 descreve as estruturas de decodificação usadas para os seguintes padrões de vídeo:

-   ITU-T Rec. H. 261
-   ITU-T Rec. H. 263
-   Vídeo MPEG-1
-   Vídeo de perfil principal MPEG-2

As especificações a seguir definem as extensões de DXVA para outros padrões de vídeo:

-   [Especificação de DXVA para decodificação H. 264/AVC](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [Especificação de DXVA para o MVC (código de vídeo MultiView) de H. 264/MPEG-4 AVC, incluindo o perfil alto estéreo](https://www.microsoft.com/download/details.aspx?id=25200)
-   [Especificação de DXVA para MPEG-1 VLD e decodificação de vídeo combinado MPEG-1/MPEG-2 VLD](https://www.microsoft.com/download/details.aspx?id=9374).
-   [Especificação de DXVA para o modo de Off-Host VLD para a decodificação de vídeo MPEG-4 parte 2](https://www.microsoft.com/download/details.aspx?id=21100)
-   [Especificação de DXVA para vídeo do Windows Media® V8, V9 e vA decodificação (incluindo SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [Especificação de DXVA (DirectX Video Acceleration) para H. 264/MPEG-4 Scalable Video CODIFICATION (SVC) Off-Host decodificação do modo VLD](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [Especificação de aceleração de vídeo DirectX para codificação de vídeo VP8 e VP9](https://www.microsoft.com/download/details.aspx?id=49188)

O DXVA 1 e o DXVA 2 usam as mesmas estruturas de dados para decodificação. No entanto, o procedimento para configurar a sessão de decodificação foi alterado. O DXVA 1 usa um mecanismo de "investigação e bloqueio", no qual o decodificador de host pode testar várias configurações antes de definir a configuração desejada no acelerador. No DXVA 2, o acelerador retorna uma lista de configurações com suporte e o decodificador de host seleciona um na lista. Os detalhes são fornecidos nas seguintes seções:

-   [Suporte a DXVA 2,0 no DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Suporte a DXVA 2,0 no Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Especificação de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
