---
description: 'Há vários formatos nos quais os dados de tinta podem ser armazenados, incluindo:'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Formatos de dados de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ccd0ab298e183867a9c4f8018727f22e51e7bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296213"
---
# <a name="ink-data-formats"></a>Formatos de dados de tinta

Há vários formatos nos quais os dados de tinta podem ser armazenados, incluindo:

-   Formato serializado da tinta (ISF)
-   HTML
-   RTF (Formato Rich Text)
-   Formato binário
-   Formatos baseados em linguagem XML (XML)

Formatos diferentes são aplicáveis em circunstâncias diferentes. Para interagir com mais sucesso com a área de transferência, os aplicativos devem ser capazes de reconhecer e gerar o máximo possível de formatos diferentes.

O formato mais importante e básico que pode ser usado para armazenar a tinta é o ISF (Ink serializado Format). O ISF fornece uma representação compacta, mas completa, de um único objeto de [**tinta**](inkdisp-class.md) .

Um formato igualmente importante é HTML. Os dados de tinta podem ser representados em HTML de forma que possam ser exibidos como uma imagem por aplicativos que não reconhecem tinta. Além disso, a fidelidade total da tinta é mantida. Por esses motivos, e como é um formato comumente compreendido que permite a representação de muitos tipos diferentes de conteúdo, a Microsoft recomenda o HTML como o formato para o compartilhamento de tinta.

Também é possível armazenar tinta em outros formatos. Usando RTF como o formato, você pode colar a tinta em aplicativos que não reconhecem tinta, como o Microsoft Word 2002. Isso é feito inserindo objetos OLE que contêm tinta no RTF. Outros formatos, como formatos binários ou baseados em XML, podem ser usados.

Os formatos que você escolhe para um determinado aplicativo para copiar, colar ou serializar tinta devem se basear em requisitos e recursos específicos de aplicativos. No mínimo, um aplicativo deve ser capaz de copiar e colar ISF, o que permite o nível mais baixo de interoperabilidade de tinta. Tanto o ISF quanto a capacidade de copiar e colar ISF são criados na plataforma do Tablet PC. No entanto, muitos aplicativos precisam representar conteúdo mais complexo, como uma seleção que contém vários objetos de tinta ou texto formatado. Nesse caso, um aplicativo pode copiar e colar HTML. Isso permite uma quantidade máxima de flexibilidade. O HTML é amplamente compreendido e fácil de gerar. Por fim, os aplicativos que já produzem RTF ou que têm uma forte necessidade de se comunicar com aplicativos mais antigos também devem produzir um formato RTF.

> [!Note]  
> Durante a discussão sobre interoperabilidade de tinta, bitmap, ISF e GIF são formatos de imagem. O objeto de tinta de texto (tInk) e o objeto de tinta de esboço (coletor) são objetos OLE. Binary, HTML, XML e RTF são formatos de documento nos quais as imagens são consumidas.

 

A plataforma do Tablet PC fornece APIs para ajudá-lo a gerar e interpretar esses formatos. Há muitas opções que juntas devem atender às necessidades de interoperabilidade e persistência de qualquer aplicativo. Para obter mais informações sobre formatos de tinta, consulte [formatos de persistência](persistence-formats.md).

 

 



