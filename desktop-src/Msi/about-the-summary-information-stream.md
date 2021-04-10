---
description: O fluxo de informações de Resumo contém informações sobre o pacote que podem ser exibidas por meio do Microsoft Windows Explorer.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Sobre o fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091551"
---
# <a name="about-the-summary-information-stream"></a>Sobre o fluxo de informações de resumo

O fluxo de informações de Resumo contém informações sobre o pacote que podem ser exibidas por meio do Microsoft Windows Explorer. Essas informações podem ser acessadas por meio da interface **IStream** . Cabe ao autor fornecer os valores para cada uma dessas propriedades.

O fluxo de informações de resumo usa COM para fornecer armazenamento estruturado de bancos de dados. O COM dá suporte ao conceito de armazenamento estruturado acessível por meio da interface **IStream** . O armazenamento estruturado, por sua vez, dá suporte ao conceito de conjuntos de propriedades como um método flexível para serialização de quase todas as informações. A especificação COM define um único conjunto de propriedades padrão, informações resumidas, que é usado para popular folhas de propriedades visíveis no Windows Explorer. Portanto, as informações armazenadas no fluxo de informações de resumo podem ser exibidas pelos usuários quando clicam com o botão direito do mouse em um banco de dados do instalador ou em uma transformação e selecionam [Propriedades](about-properties.md).

Para obter uma lista do conjunto de propriedades de resumo, consulte [resumir informações de fluxo conjunto de propriedades](summary-information-stream-property-set.md).

Para obter descrições breves das propriedades de informações resumidas usadas com bancos de dados, transformações e patches, consulte [descrições de propriedades de resumo](summary-property-descriptions.md).

 

 



