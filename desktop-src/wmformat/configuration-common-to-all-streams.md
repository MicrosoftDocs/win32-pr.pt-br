---
title: configuração comum a todos os Fluxos
description: configuração comum a todos os Fluxos
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- perfis, configurações comuns a todos os fluxos
- fluxos, configurações comuns
- fluxos, nomes
- fluxos, nomes de conexão
- fluxos, números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e8b58e97ce2add4b6ff139aebacbc6d510af4424b2d3ae2bff3ea4577c429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964175"
---
# <a name="configuration-common-to-all-streams"></a>configuração comum a todos os Fluxos

Todos os fluxos, independentemente do tipo, devem ser atribuídos a um nome de fluxo, um nome de conexão e um número de fluxo.

O nome do fluxo é simplesmente um nome descritivo que você atribui ao fluxo. Um fluxo não precisa ter um nome de fluxo, mas ajuda a identificar o fluxo ao editar o perfil posteriormente. Você pode definir um nome para o fluxo chamando [**IWMStreamConfig:: Setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).

Cada fluxo deve ter um nome de conexão, também chamado de nome de entrada. Quando você define o perfil no objeto do gravador para gravar um arquivo, o gravador associará cada nome de conexão a uma entrada. Para identificar as entradas, você deve chamar [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) para recuperar o nome da conexão. Nomes de conexão típicos são descrições simples do conteúdo, como "áudio". Se o seu perfil contiver fluxos mutuamente exclusivos por taxa de bits, cada um dos fluxos mutuamente exclusivos deverá ter o mesmo nome de conexão. Se não tiverem, o perfil será inválido e será rejeitado pelo gravador. Você pode definir um nome de conexão chamando [**IWMStreamConfig:: Setconnectionname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).

O número do fluxo identifica o fluxo dentro do arquivo. Ao contrário dos números de entrada e de saída, os números de fluxo começam em 1, e não 0. Um número de fluxo é diferente de um índice de fluxo, que você usa ao obter fluxos em um perfil usando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream). O índice de fluxo é um número atribuído ao fluxo pelo objeto de perfil. Os índices de fluxo variam entre 0 e um menor que o número de fluxos recuperados por [**IWMProfile:: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount). Os números de fluxo não precisam ser sequenciais, embora normalmente estejam e podem variar de 1 a 63. Você pode definir um número de fluxo chamando [**IWMStreamConfig:: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configurando Fluxos**](configuring-streams.md)
</dt> <dt>

[**entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




