---
title: Objeto do editor de metadados
description: Objeto do editor de metadados
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows SDK de Formato de Mídia, objetos do editor de metadados
- FORMATO DE SISTEMAS Avançados (ASF), objetos do editor de metadados
- ASF (Formato de Sistemas Avançados), objetos do editor de metadados
- objetos, objetos do editor de metadados
- objetos do editor de metadados, sobre
- metadados, objetos do editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8e78aaf6ada96a9cefa1a9ec6f4aa5708c7382539bc3b75493734c18d600b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027444"
---
# <a name="metadata-editor-object"></a>Objeto do editor de metadados

O objeto do editor de metadados é usado para editar informações armazenadas na seção de header de arquivos ASF. As coisas mais comuns manipuladas por esse objeto são atributos de metadados. Além disso, o editor de metadados lida com [*marcadores e*](wmformat-glossary.md) comandos de script. A única vez que você precisa usar o editor de metadados é quando deseja editar o header de um arquivo existente sem reprodução.

O objeto do editor de metadados é criado pela função [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), que define um ponteiro para uma interface **IWMMetadataEditor.** As outras interfaces do objeto do editor de metadados podem ser obtidas chamando **o método QueryInterface.**

As interfaces a seguir têm suporte no objeto do editor de metadados.



| Interface                                        | Descrição                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Permite que os aplicativos de edição examinem as propriedades [*drm*](wmformat-glossary.md) de um arquivo ASF sem ter direitos para reproduzir o conteúdo protegido. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Manipula atributos, marcadores e comandos de script no header.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Recupera informações de codec. Herda todos os métodos de **IWMHeaderInfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Fornece suporte avançado para atributos, incluindo atributos grandes, vários idiomas e nomes de atributo duplicados. Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Abre, fecha e salva as alterações no header de um arquivo ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Abre um arquivo ASF para edição de header com várias opções de acesso a arquivos e compartilhamento. Herda todos os métodos de **IWMMetadataEditor**.                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Marcadores**](markers.md)
</dt> <dt>

[**Metadados**](metadata.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




