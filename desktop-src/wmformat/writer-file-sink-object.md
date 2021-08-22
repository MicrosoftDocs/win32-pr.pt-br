---
title: Objeto de coletor de arquivo do gravador
description: Objeto de coletor de arquivo do gravador
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows SDK de Formato de Mídia, objetos de sink de arquivo de autor
- FORMATO DE SISTEMAS Avançados (ASF), objetos de sink de arquivo de autor
- ASF (Formato de Sistemas Avançados), objetos de sink de arquivo de autor
- objetos, objetos do sink do arquivo de autor
- objetos do sink do arquivo de writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08efb5c404a822b0c30747864bdc01f57cb1a0618eed3f7ad26bd92f158ba625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083640"
---
# <a name="writer-file-sink-object"></a>Objeto de coletor de arquivo do gravador

O objeto do sink do arquivo de autor é usado ao escrever Windows de mídia em um arquivo.

O objeto do sink do arquivo de autor é criado pela função [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), que define um ponteiro para uma interface **IWMWriterFileSink.** As outras interfaces do objeto do sink do arquivo de autor podem ser obtidas chamando **o método QueryInterface.**

As interfaces a seguir são suportadas pelo objeto de sink de arquivo do writer.



| Interface                                          | Descrição                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que o aplicativo receba mensagens de status do objeto .                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Abre um arquivo no qual o objeto de gravação pode gravar dados.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Fornece gerenciamento estendido de um objeto de sink de arquivo. Herda todos os métodos de **IWMWriterFileSink.**                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Fornece opções adicionais para escrever arquivos. Herda todos os métodos de **IWMWriterFileSink** e **IWMWriterFileSink2**. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Aloca memória, determina se o sink está operando em tempo real e lida com várias funções de retorno de chamada.                |



 

A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para acompanhar o progresso de um objeto de sink de arquivo de autor.



| Interface                                      | Descrição                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Necessário quando as informações de status devem ser comunicadas ao aplicativo host. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




