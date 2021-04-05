---
title: Fluxos da Web
description: Fluxos da Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- SDK do Windows Media Format, Web streams
- ASF (Advanced Systems Format), fluxos da Web
- ASF (formato de sistemas avançados), fluxos da Web
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- Fluxos da Web, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005447"
---
# <a name="web-streams"></a>Fluxos da Web

Um fluxo da Web é como um fluxo de arquivos, pois ele contém arquivos de dados. Em um fluxo da Web, esses arquivos normalmente são páginas HTML e elementos gráficos associados no formato GIF ou JPEG.

Os fluxos da Web podem ser particularmente úteis para arquivos ASF que são usados como apresentações. Antes do suporte de fluxos da Web, as apresentações teriam URLs em fluxos de script em um arquivo para que uma página da Web fosse carregada em um tempo predeterminado. A dificuldade era que o congestionamento da rede poderia causar atrasos e criar uma experiência de exibição ruim.

Com os fluxos da Web, as partes constituintes de páginas da Web podem ser incluídas no arquivo ASF como um fluxo. À medida que os arquivos são recebidos, eles podem ser armazenados em cache para que, quando o comando para exibir (ou renderizar) uma URL seja entregue, eles possam ser acessados instantaneamente por um navegador. Isso permite uma reprodução uniforme e consistente. O comando render é entregue no fluxo da Web em si, não como um comando de script em um fluxo separado.

É recomendável que os fluxos da Web criados usando o SDK da série Windows Media Format 9 Series ou posterior recebam o número de versão 1. Esse valor é especificado na estrutura [**de \_ \_ formato webstream do WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) no membro **wVersion** . O próprio SDK não faz nada para impor essa versão.

> [!Note]  
> Ao se conectar a fluxos de transmissão ao vivo que têm fluxos da Web, é possível que o usuário receba um comando render antes que o arquivo especificado esteja realmente no cache local. A menos que seu aplicativo manipule essa condição, o navegador exibirá um erro "página não encontrada".

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos arbitrários**](arbitrary-streams.md)
</dt> <dt>

[**Configurando fluxos da Web**](configuring-web-streams.md)
</dt> </dl>

 

 




