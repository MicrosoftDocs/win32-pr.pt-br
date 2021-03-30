---
title: Criando objetos vinculados e incorporados de dados existentes
description: Criando objetos vinculados e incorporados de dados existentes
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637157"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a>Criando objetos vinculados e incorporados de dados existentes

Normalmente, um usuário monta um documento composto usando a área de transferência ou arrasta e solta para copiar um objeto de dados de seu aplicativo de servidor para o aplicativo de contêiner do usuário. Com aplicativos que dão suporte ao OLE, o usuário pode iniciar a transferência do servidor ou do contêiner. Por exemplo, o servidor pode copiar dados para a área de transferência no aplicativo de servidor e, em seguida, alternar para o aplicativo de contêiner e escolher colar objeto especial/inserido ou um comando de menu equivalente para criar um novo objeto inserido a partir dos dados selecionados. Ou, o usuário pode arrastar os dados de um aplicativo para o outro. O processo é semelhante para a criação de um objeto vinculado.

> [!Note]  
> Um aplicativo que funciona como servidor OLE e contêiner pode usar uma seleção de seus próprios dados para criar um objeto incorporado ou vinculado em um novo local dentro do mesmo documento.

 

A transferência de dados entre o servidor OLE e os aplicativos de contêiner é criada na transferência de dados uniforme, conforme descrito em [transferência de dados](data-transfer.md). Os servidores OLE e manipuladores de objeto implementam [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para disponibilizar seus dados para transferências usando a área de transferência ou arrastar e soltar. Os objetos OLE dão suporte a todos os formatos de área de transferência usual. Além disso, eles dão suporte a seis formatos de área de transferência que dão suporte à criação de objetos vinculados e incorporados de um objeto de dados selecionado.

Os formatos de área de transferência OLE descrevem os objetos de dados que, ao serem descartados ou colados em contêineres OLE, devem se tornar objetos compostos ou vinculados ao documento composto. O objeto de dados apresenta esses formatos aos aplicativos de contêiner em ordem de fidelidade como descrições dos dados. Em outras palavras, o objeto apresenta primeiro o formato que o representa melhor, seguido pelo seguinte formato melhor e assim por diante. Essa ordenação intencional incentiva um aplicativo de contêiner a usar o melhor formato possível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> <dt>

[Transferência de Dados](data-transfer.md)
</dt> </dl>

 

 




