---
title: Transferência de dados
description: Transferência de dados
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498803"
---
# <a name="data-transfer"></a>Transferência de dados

O COM (Component Object Model) fornece um mecanismo padrão para transferir dados entre aplicativos. Esse mecanismo é o *objeto de dados*, que é simplesmente qualquer objeto com que implementa a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Alguns objetos de dados, como uma parte do texto copiado para a área de transferência, têm **IDataObject** como sua única interface. Outros, como objetos de documento compostos, expõem várias interfaces, das quais **IDataObject** é simplesmente um. Os objetos de dados são fundamentais para o trabalho de documentos compostos, embora também tenham um aplicativo generalizado fora dessa tecnologia OLE.

Ao trocar ponteiros para um objeto de dados, os provedores e consumidores de dados podem gerenciar transferências de dados de maneira uniforme, independentemente do formato dos dados, do tipo de mídia usado para transferir os dados ou do dispositivo de destino no qual ele deve ser renderizado. Você pode incluir o suporte em seu aplicativo para transferências de área de transferência básica, arrastar e soltar transferências e transferências de documentos compostos OLE com uma única implementação de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). Tendo feito isso, a quantidade de código necessária para acomodar a semântica especial de cada protocolo é mínima.

Para mais informações, consulte os seguintes tópicos:

-   [Interfaces Transferência de Dados](data-transfer-interfaces.md)
-   [Formatos de dados e mídia de transferência](data-formats-and-transfer-media.md)
-   [Arrastar e soltar](drag-and-drop.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 




