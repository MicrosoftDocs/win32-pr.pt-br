---
title: Para editar metadados com o gravador
description: Para editar metadados com o gravador
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- SDK do Windows Media Format, editando metadados com o gravador
- SDK do Windows Media Format, edição de metadados
- ASF (Advanced Systems Format), editando metadados com o gravador
- ASF (formato de sistemas avançados), editando metadados com o gravador
- ASF (Advanced Systems Format), edição de metadados
- ASF (formato de sistemas avançados), edição de metadados
- metadados, edição com o gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365755"
---
# <a name="to-edit-metadata-with-the-writer"></a>Para editar metadados com o gravador

Você pode acessar o, diretamente do gravador, os metadados que vão para o cabeçalho do arquivo. Chame o método **QueryInterface** de qualquer interface no objeto do gravador para obter um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) . Depois de ter um ponteiro para a interface apropriada, você poderá manipular os metadados da mesma forma que faria se tivesse carregado o arquivo no objeto editor de metadados. Para obter mais informações sobre como editar metadados, consulte [trabalhando com metadados](working-with-metadata.md).

Você deve fazer todas as alterações nos metadados antes de chamar [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

> [!Note]  
> Se você definir metadados para um arquivo, gravar o arquivo e, em seguida, se preparar para gravar um novo arquivo sem liberar o gravador, alguns metadados que foram definidos para o primeiro arquivo permanecerão definidos e serão incluídos nos arquivos subsequentes. Ao gravar vários arquivos com a mesma instância do objeto Writer, você tem duas opções: verificar todos os metadados antes de gravar cada arquivo ou apenas gravar os metadados do gravador que se aplicam a todos os arquivos que você está gravando.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




