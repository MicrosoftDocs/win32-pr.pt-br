---
description: O formato de fonte OpenType baseado em Unicode estende o formato de arquivo de fonte TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato de fonte OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751218"
---
# <a name="opentype-font-format"></a>Formato de fonte OpenType

O formato de fonte OpenType baseado em Unicode estende o formato de arquivo de fonte TrueType. As fontes OpenType permitem o mapeamento entre os caracteres e os [glifos](uniscribe-glossary.md), habilitando o suporte para ligaturas, formas posicionais, alternativas e outras substituições. As fontes OpenType também podem incluir informações que dão suporte a posicionamento de glifo bidimensional e anexo de glifo e podem conter contornos TrueType ou PostScript.

Os recursos de layout em fontes OpenType são organizados por scripts e linguagens, permitindo que uma única fonte dê suporte a vários sistemas de escrita, mesmo no mesmo script. Para garantir a consistência nas operações de layout de texto e evitar sobrecarga desnecessária em arquivos de fonte ou aplicativos, muitos dos algoritmos de layout de texto e de linguagem de idioma são incluídos no Uniscribe. Isso alivia o desenvolvedor de fontes de ter que definir regras de script generalizadas dentro de uma fonte.

Os aplicativos podem introduzir conhecimento ou preferências específicas sobre o layout do script. Fontes de layout OpenType podem até mesmo conter regras de layout que duplicam ou substituem as aplicadas pelos serviços do sistema operacional. A estrutura em camadas dos serviços do sistema operacional que dá suporte ao layout de texto permite que um aplicativo escolha as informações de layout a serem usadas e selecione como aplicá-las. Para obter informações adicionais, consulte a [visão geral das especificações do Microsoft Typography](https://www.microsoft.com/typography/SpecificationsOverview.mspx) ou a [especificação OpenType](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



