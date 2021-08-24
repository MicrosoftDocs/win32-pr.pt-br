---
description: O formato de fonte OpenType baseado em Unicode estende o formato de arquivo de fonte TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato de fonte OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18324f3a9c84553da81c9f9723a2ecd67c03539b4dd39c7a80afc4be5cdcda66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147089"
---
# <a name="opentype-font-format"></a>Formato de fonte OpenType

O formato de fonte OpenType baseado em Unicode estende o formato de arquivo de fonte TrueType. As fontes OpenType permitem o mapeamento entre caracteres e [glifos,](uniscribe-glossary.md)habilitando o suporte para ligaduras, formulários posicionais, alternativas e outras substituições. As fontes OpenType também podem incluir informações que suportam posicionamento de glifo bidimensional e anexo de glifo e podem conter trueType ou estruturas PostScript estruturas.

Os recursos de layout em fontes OpenType são organizados por scripts e linguagens, permitindo que uma única fonte de suporte a vários sistemas de escrita, mesmo dentro do mesmo script. Para garantir a consistência em operações de layout de texto e evitar sobrecarga desnecessária em arquivos de fonte ou aplicativos, muitos dos algoritmos semânticos de idioma e layout de texto são incluídos no Uniscribe. Isso alivia o desenvolvedor de fontes de precisar definir regras de script generalizadas dentro de uma fonte.

Os aplicativos podem introduzir conhecimento ou preferências específicos sobre o layout do script. As fontes de layout OpenType podem até mesmo conter regras de layout que duplicam ou superam as aplicadas pelos serviços do sistema operacional. A estrutura em camadas dos serviços do sistema operacional que dá suporte ao layout de texto permite que um aplicativo escolha as informações de layout a usar e selecione como aplicá-la. Para obter informações adicionais, consulte a [Visão geral das Especificações](https://www.microsoft.com/typography/SpecificationsOverview.mspx) de Tipografia da Microsoft ou a [Especificação OpenType](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



