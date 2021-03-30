---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, migrando DVDs
- Modelo de objeto do Windows Media Player, DVDs
- modelo de objeto, DVDs
- Controle ActiveX do Windows Media Player, DVDs
- Controle ActiveX, DVDs
- Controle ActiveX móvel do Windows Media Player, DVDs
- Windows Media Player Mobile, migrando DVDs
- Guia de migração, DVDs
- Migração de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636277"
---
# <a name="dvd"></a>DVD

O controle ActiveX do Windows Media Player 6,4 contém um objeto de **DVD** que expõe uma variedade de métodos e propriedades e um evento, para lidar especificamente com conteúdo de DVD. Por exemplo, para determinar o número de títulos de DVD disponíveis, use o **Player6**. Propriedade **titlesAvailable** :


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



O modelo de objeto do Windows Media Player 7 ou posterior implementa uma abordagem mais integrada ao DVD. Propriedades, métodos e eventos específicos de DVD são implementados somente quando necessário. Caso contrário, a funcionalidade de modelo de objeto existente funciona com mídia de DVD como você pode esperar. Por exemplo, para determinar o número de títulos de DVD disponíveis ao usar o Windows Media Player 7 ou posterior, você recupera um objeto de **playlist** do objeto de **cdrom** :


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



O exemplo anterior recupera um objeto de **playlist** com uma primeira entrada que representa a mídia de DVD na primeira unidade. Entradas adicionais representam títulos de DVD individuais. Portanto, o número de títulos disponíveis pode ser calculado da seguinte maneira:


```C++
var numTitles = dvdTitles.count - 1;

```



Aqui estão as principais diferenças a serem consideradas ao migrar da versão 6,4:

-   A reprodução de DVD tem suporte apenas ao usar o Windows Media Player para Windows XP ou posterior e o sistema operacional Windows XP ou posterior.
-   As unidades de DVD-ROM são enumeradas exatamente como unidades de CD-ROM usando o objeto **cdromCollection** .
-   Unidades de DVD-ROM individuais são gerenciadas usando o objeto **cdrom** .
-   O objeto **DVD** estende o modelo de objeto com métodos e uma propriedade especificamente para trabalhar com o DVD.
-   Há dois novos eventos, **OpenPlaylistSwitch** e **DomainChange**, especificamente para trabalhar com DVD.
-   O conteúdo do DVD é organizado usando objetos de **lista de reprodução** e objetos de **mídia** .
-   As linguagens de DVD são gerenciadas usando a funcionalidade de linguagem disponível no objeto de **controles** (Windows Media Player 9 Series ou posterior).
-   Os controles de transporte e as informações de posição para DVD funcionam da mesma forma que para outros tipos de mídia digital.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> <dt>

[**Usando o controle do Windows Media Player com Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




