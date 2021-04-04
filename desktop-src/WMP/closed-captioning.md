---
title: Legendagem oculta
description: Legendagem oculta
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Windows Media Player, migrando legendas ocultas
- Modelo de objeto do Windows Media Player, legendas codificadas do Smigrating
- modelo de objeto, migrando legendas ocultas
- Windows Media Player Mobile, migrando legendas ocultas
- Controle ActiveX do Windows Media Player, migrando legendas ocultas
- Controle ActiveX móvel do Windows Media Player, migrando legendas ocultas
- Controle ActiveX, migrando legendas ocultas
- SAMI (intercâmbio de mídia acessível) sincronizado, migrando legendas ocultas
- SAMI (sincronizado com o intercâmbio de mídia acessível), migrando legendas ocultas
- Guia de migração, SAMI (sincronização de mídia acessível)
- Guia de migração, legendagem oculta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084376"
---
# <a name="closed-captioning"></a>Legendagem oculta

O controle ActiveX do Windows Media Player 6,4 inclui um painel de exibição de legenda oculta integrada que, quando torna-se visível, habilita legendas codificadas SAMI (intercâmbio de mídia acessível) e exibe o texto da legenda oculta. O controle Windows Media Player 7 ou posterior habilita a exibição da legenda fechada do SAMI usando um **<DIV>** elemento HTML. Por exemplo:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Essa técnica oferece flexibilidade total, já que você pode criar sua página da Web para exibir legendas ocultas de uma maneira personalizada; a exibição de legenda oculta não precisa mais estar em um local fixo adjacente à interface do usuário do Windows Media Player.

Depois de criar uma área para exibir legendas codificadas, use o *ClosedCaption*. Propriedade **captioningID** para especificar o local em que o Windows Media Player renderiza o texto da legenda oculta.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



O SDK (Software Development Kit) do Windows Media Player contém um exemplo funcional de um player incorporado que exibe texto de legenda oculta. Para obter as amostras do SDK, baixe e instale o SDK completo do Windows Media Player no site da Microsoft. Para obter mais informações sobre legendas codificadas e SAMI, consulte o [site de acessibilidade da Microsoft](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




