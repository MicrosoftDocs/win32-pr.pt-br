---
title: Arquivos de arte
description: Arquivos de arte
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Windows Media Player capas, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89ccf07757e511f7717cbe3bbeff2cdacee004da8d3b64d27ddcef7ae2199a29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956366"
---
# <a name="art-files"></a>Arquivos de arte

Você deve criar um ou mais arquivos de arte para sua capa. Sem arte, o usuário não terá nada a ver. Você poderia criar uma capa invisível, mas ninguém verá! E mesmo assim, você ainda precisaria criar arquivos Art para manter suas imagens invisíveis, pois o arquivo de definição de capa requer arquivos Art para elementos específicos.

Há três usos para arte em capas: imagens primárias, imagens de mapeamento e imagens alternativas.

## <a name="primary-images"></a>Imagens primárias

Você deve criar uma imagem primária para sua capa. Isso é o que os usuários verão quando instalarem sua capa. A imagem primária é composta de uma ou mais imagens que são criadas por controles de capa específicos.

Se você tiver mais de um controle, deverá especificar a ordem z, que define quais controles são exibidos na frente de outros controles. Cada elemento de **exibição** terá uma imagem de plano de fundo à qual você pode adicionar outras imagens de elemento, permitindo que você crie uma imagem composta primária.

Você também pode ter imagens secundárias, como uma bandeja deslizante, que não são exibidas quando sua aparência é exibida pela primeira vez, mas que aparecem quando o usuário executa alguma ação. Eles seguem as mesmas regras que as imagens primárias, pois elas são criadas com um conjunto de controles.

## <a name="mapping-images"></a>Mapeando imagens

um dos recursos mais poderosos das capas Windows Media Player é que você pode usar o mapeamento de imagem para disparar eventos para sua capa. Mapas de imagem são arquivos que contêm imagens especiais. as imagens em um arquivo de mapa de imagem, no entanto, não devem ser exibidas pelo usuário, mas são usadas pelo Windows Media Player para executar uma ação quando o usuário clica em sua capa.

Controles diferentes precisam de diferentes tipos de mapas de imagem. Por exemplo, se você colorir parte de um mapa de imagem de um valor vermelho específico e o usuário clicar na área correspondente da imagem primária, um botão acionará um evento. A cor é usada para definir quais eventos são disparados clicando em uma área específica da capa.

## <a name="alternate-images"></a>Imagens alternativas

Você também pode configurar imagens alternativas para exibir quando um usuário faz algo. Por exemplo, você pode criar uma imagem alternativa de um botão que será exibido somente quando o mouse passar sobre o botão. Essa é uma boa maneira de permitir que os usuários saibam o que eles podem fazer e também permite uma interface do usuário altamente detectável. Usando dicas de ferramentas e focalizar imagens com cuidado, você pode criar interfaces de usuário incomuns que ainda dão ao usuário comentários sobre quais opções estão disponíveis.

As seções a seguir fornecem mais informações sobre arquivos de arte:

-   [Imagens primárias](primary-images.md)
-   [Mapeando imagens](mapping-images.md)
-   [Imagens alternativas](alternate-images.md)
-   [Formatos de arquivo artístico](art-file-formats.md)
-   [Exemplo de arte simples](simple-art-example.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de capa**](skin-files.md)
</dt> </dl>

 

 




