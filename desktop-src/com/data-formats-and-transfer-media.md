---
title: Formatos de dados e mídia de transferência
description: Formatos de dados e mídia de transferência
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccbab96fbaca83330737521f253b3c625e67ea9a024d87d35276da2826a3964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501426"
---
# <a name="data-formats-and-transfer-media"></a>Formatos de dados e mídia de transferência

A maioria das plataformas, incluindo o Windows, define um protocolo padrão para transferir dados entre aplicativos, com base em um conjunto de funções chamado de área de transferência. Os aplicativos que usam essas funções podem compartilhar dados mesmo que seus formatos de dados nativos sejam indiferentemente diferentes. Em geral, essas áreas de transferência têm duas falhas significativas que o COM supera.

Primeiro, as descrições de dados usam apenas um identificador de formato, como o identificador de formato de área de transferência de 16 bits único no Windows, o que significa que a área de transferência só pode descrever a estrutura de seus dados, ou seja, a ordem dos bits. Ele pode relatar, "tenho um bitmap" "ou ter algum texto," mas não pode especificar os dispositivos de destino para os quais os dados são compostos, quais modos de exibição ou aspectos de si mesmos os dados podem fornecer, ou quais mídias de armazenamento são mais adequadas para sua transferência. Por exemplo, ele não pode relatar: "tenho uma cadeia de texto que é armazenada na memória global e formatada para apresentação na tela ou em uma impressora" ou "tenho um bitmap de esboço em miniatura renderizado para uma impressora matricial de ponto de 100 dpi e armazenado como um arquivo de disco".

Em segundo lugar, todas as transferências de dados que usam a área de transferência geralmente ocorrem por meio da memória global. O uso da memória global é razoavelmente eficiente para pequenas quantidades de dados, mas terrivelmente ineficiente para grandes quantidades, como um objeto multimídia de 20 MB. A memória global está lenta para um objeto de dados grande, cujo tamanho requer uma troca considerável na memória virtual no disco. Nos casos em que os dados que estão sendo trocados vão residir principalmente no disco de qualquer forma, forçá-lo por meio desse afunilamento de memória virtual é altamente ineficiente. Uma maneira melhor seria ignorar totalmente a memória global e simplesmente transferir os dados diretamente para o disco.

Para aliviar esses problemas, o COM fornece duas estruturas de dados: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Para obter mais informações, consulte estes tópicos:

-   [A estrutura FORMATETC](the-formatetc-structure.md)
-   [A estrutura STGMEDIUM](the-stgmedium-structure.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de dados](data-transfer.md)
</dt> </dl>

 

 




