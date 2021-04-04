---
title: Objeto de coletor de arquivo do gravador
description: Objeto de coletor de arquivo do gravador
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- SDK do Windows Media Format, objetos do coletor de arquivo do Writer
- ASF (Advanced Systems Format), objetos de coletor de arquivo do Writer
- ASF (formato de sistemas avançados), objetos do coletor de arquivo do gravador
- objetos, objetos do coletor de arquivo do gravador
- objetos do coletor de arquivo do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007246"
---
# <a name="writer-file-sink-object"></a>Objeto de coletor de arquivo do gravador

O objeto de coletor de arquivo do gravador é usado ao gravar a saída do Windows Media em um arquivo.

O objeto de coletor de arquivo do gravador é criado pela função [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), que define um ponteiro para uma interface **IWMWriterFileSink** . As outras interfaces do objeto de coletor de arquivo do gravador podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto de coletor de arquivo do gravador.



| Interface                                          | Descrição                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que o aplicativo obtenha mensagens de status do objeto.                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Abre um arquivo no qual o objeto gravador pode gravar dados.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Fornece gerenciamento estendido de um objeto de coletor de arquivos. Herda todos os métodos de **IWMWriterFileSink**.                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Fornece opções adicionais para gravar arquivos. Herda todos os métodos de **IWMWriterFileSink** e **IWMWriterFileSink2**. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Aloca memória, determina se o coletor está operando em tempo real e manipula várias funções de retorno de chamada.                |



 

A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para acompanhar o progresso de um objeto de coletor de arquivo do gravador.



| Interface                                      | Descrição                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Necessário quando as informações de status devem ser comunicadas ao aplicativo host. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




