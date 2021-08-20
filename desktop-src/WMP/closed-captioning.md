---
title: Legenda fechada
description: Legenda fechada
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player de objeto, SAMI (Synchronized Accessible Media Interchange)
- modelo de objeto, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Controle ActiveX dispositivo móvel, SAMI (Synchronized Accessible Media Interchange)
- ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player, migrando legendas fechadas
- Windows Media Player modelo de objeto, Migrando legendas fechadas
- modelo de objeto, migrando legendas fechadas
- Windows Media Player Móvel, migrando legendas fechadas
- Windows Media Player ActiveX controle, migrando legendas fechadas
- Windows Media Player Controle ActiveX dispositivo móvel, migrando legendas fechadas
- ActiveX controle, migrando legendas fechadas
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), migrando legendas fechadas
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), migrando legendas fechadas
- guia de migração,SAMI (Synchronized Accessible Media Interchange)
- guia de migração, legenda fechada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa83cb5fb6735475a883986673c958db9642386bd8ce2c76151ddd6c2f23ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119589"
---
# <a name="closed-captioning"></a>Legenda fechada

O controle Windows Media Player 6.4 ActiveX inclui um painel de exibição de legenda fechada integrado que, quando visível, habilita legendas fechadas sami (intercâmbio de mídia acessível sincronizado) e exibe o texto de legenda fechado. O Windows Media Player 7 ou posterior habilita a exibição de legenda fechada SAMI usando um elemento **<DIV>** HTML. Por exemplo:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Essa técnica fornece flexibilidade total, pois você pode projetar sua página da Web para exibir legendas fechadas de maneira personalizada; A exibição de legenda fechada não é mais necessária para estar em um local fixo adjacente à interface do Windows Media Player usuário.

Depois de criar uma área para exibir legendas fechadas, use *ClosedCaption*. **propriedade captioningID** para especificar o local em que Windows Media Player renderiza o texto de legenda fechado.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



O Windows Media Player SDK (Software Development Kit) contém um exemplo de trabalho de um Player inserido que exibe o texto de legenda fechado. Para obter os exemplos do SDK, baixe e instale o SDK Windows Media Player completo do Site da Microsoft. Para obter mais informações sobre legendas fechadas e SAMI, consulte o [site Microsoft Accessibility](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guia de migração de modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




