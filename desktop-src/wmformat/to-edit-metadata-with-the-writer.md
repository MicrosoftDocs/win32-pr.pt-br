---
title: Para editar metadados com o writer
description: Para editar metadados com o writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows SDK de Formato de Mídia, editando metadados com o autor
- Windows SDK de Formato de Mídia, edição de metadados
- ASF (Advanced Systems Format), editando metadados com o autor
- ASF (Formato de Sistemas Avançados), editando metadados com o autor
- ASF (Advanced Systems Format), edição de metadados
- ASF (Formato de Sistemas Avançados), edição de metadados
- metadados, edição com o autor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d09db09a2cd7dbc50130243e322085ab2113e76f71d8b6760bd602d16f29d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197066"
---
# <a name="to-edit-metadata-with-the-writer"></a>Para editar metadados com o writer

Você pode acessar, diretamente do autor, os metadados que entrarão no header do arquivo. Chame o **método QueryInterface** de qualquer interface no objeto writer para obter um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) Depois de ter um ponteiro para a interface apropriada, você poderá manipular os metadados da mesma forma que faria se tivesse carregado o arquivo no objeto do editor de metadados. Para obter mais informações sobre como editar metadados, consulte [Trabalhando com metadados](working-with-metadata.md).

Você deve fazer todas as alterações nos metadados antes de chamar [**IWMWriter::BeginWriting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)

> [!Note]  
> Se você definir metadados para um arquivo, gravar o arquivo e, em seguida, preparar-se para gravar um novo arquivo sem liberar o autor, alguns metadados que foram definidos para o primeiro arquivo permanecerão definidos e serão incluídos nos arquivos subsequentes. Ao gravar vários arquivos com a mesma instância do objeto writer, você tem duas opções: verificar todos os metadados antes de gravar cada arquivo ou gravar apenas nos metadados de gravação que se aplica a todos os arquivos que você está escrevendo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




