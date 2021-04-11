---
title: Lidando com conteúdo protegido
description: Lidando com conteúdo protegido
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- aplicativos de área de trabalho, certificados
- provedores de serviços, certificados
- Guia de programação, certificados
- certificates
- Windows Media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- aplicativos de área de trabalho, provedor de conteúdo seguro (SCP)
- provedores de serviços, provedor de conteúdo seguro (SCP)
- Guia de programação, provedor de conteúdo seguro (SCP)
- provedor de conteúdo seguro (SCP)
- SCP (provedor de conteúdo seguro)
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- Guia de programação, conteúdo protegido por DRM
- aplicativos de desktop, conteúdo protegido por DRM
- provedores de serviços, conteúdo protegido por DRM
- Conteúdo protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363859"
---
# <a name="handling-protected-content"></a>Lidando com conteúdo protegido

Se você estiver criando um aplicativo ou provedor de serviços que consumirá conteúdo protegido pelo DRM (gerenciamento de direitos digitais) do Windows Media, você deverá ter um par de chave/certificado emitido pela Microsoft. Para saber onde obter esse certificado, consulte [ferramentas para desenvolvimento](tools-for-development.md). Se você não pretende manipular o conteúdo protegido, você pode usar a chave fictícia e o certificado fornecido com esse SDK em um arquivo chamado Key. c.

Para qualquer arquivo protegido pela tecnologia DRM, o Windows Media Gerenciador de Dispositivos requer a presença de um SCP (provedor de conteúdo seguro) para esse formato de arquivo. A Microsoft fornece um módulo SCP para arquivos WMA e WMV. Se seu aplicativo ou provedor de serviços estiver lidando com conteúdo protegido por DRM de outro formato, você deverá fornecer seu próprio módulo SCP. Um módulo SCP é um objeto COM que implementa todas as [interfaces para provedores de conteúdo seguro](interfaces-for-secure-content-providers.md).

Um aplicativo pode enviar conteúdo protegido por DRM para dispositivos criados no Windows Media DRM 10 para dispositivos portáteis ou em um PDDRM (DRM de dispositivo portátil). No entanto, você só pode criar um provedor de serviços para dispositivos criados em PDDRM; Você não pode criar um provedor de serviços para dispositivos criados no Windows Media DRM 10 para dispositivos portáteis. Esses últimos dispositivos só podem usar o provedor de serviços MTP fornecido pela Microsoft.

Os dispositivos criados no PDDRM só podem dar suporte a licenças para conteúdo comprado. As licenças que têm condições de expiração de tempo só têm suporte em dispositivos criados no Windows Media DRM 10 para dispositivos portáteis, que têm requisitos especiais, como um Clock e uma individualização seguros. O SDK do Windows Media DRM 10 para dispositivos portáteis fornece detalhes sobre os requisitos de dispositivo para dar suporte à tecnologia da versão 10.

Antes de enviar conteúdo de DRM para o dispositivo, um aplicativo deve verificar várias coisas:

-   Se o dispositivo dá suporte à tecnologia DRM.
-   A qual versão da tecnologia DRM ela dá suporte (versão 10 ou anterior).
-   Se o dispositivo for criado na versão 10, se todos os seus componentes estiverem atualizados (como o relógio seguro e quaisquer requisitos de individualização).

Todas as chamadas de método para responder a essas perguntas são feitas pelo cliente e manipuladas pelo Windows Media Gerenciador de Dispositivos e pelo componente do provedor de conteúdo seguro; o provedor de serviços não lida com nenhuma dessas chamadas.

Se o dispositivo não oferecer suporte ao Windows Media DRM 10 para dispositivos portáteis, ele ainda poderá consumir conteúdo protegido (dependendo da licença de conteúdo e do design do dispositivo), mas qualquer conteúdo enviado a ele terá uma licença de uso simplificada com direitos limitados (por exemplo, sem expiração de tempo).

-   Para obter exemplos que demonstram como um aplicativo verifica se um dispositivo pode lidar com conteúdo protegido e se precisa atualizar seus componentes DRM, consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md).
-   Para obter mais informações sobre como criar um provedor de serviços que possa lidar com conteúdo protegido, consulte [lidando com conteúdo protegido no provedor de serviços](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> Muitos direitos de transferência de arquivo do Windows Media Gerenciador de Dispositivos ou os métodos de solicitação de permissão falharão (geralmente com um valor de **HRESULT** misterioso) ao manipular arquivos protegidos por DRM com um depurador anexado. Portanto, você deve usar maneiras alternativas para depurar seu código, como as saídas de log para um formulário do Windows ou um arquivo de log. Para obter mais informações sobre opções de log, consulte [habilitando o log](enabling-logging.md). Se você estiver executando um depurador no conteúdo protegido, um método retornará um dos códigos de erro listados na seção DRM códigos de [erro](error-codes.md)ou, possivelmente, um código de erro desconhecido. Se você obtiver um valor misterioso de **HRESULT** ao executar um depurador em um conteúdo ou métodos protegidos, a proteção de DRM poderá ser a causa.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




