---
title: Objeto do editor de metadados
description: Objeto do editor de metadados
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- SDK do Windows Media Format, objetos do editor de metadados
- ASF (Advanced Systems Format), objetos do editor de metadados
- ASF (formato de sistemas avançados), objetos do editor de metadados
- objetos, objetos do editor de metadados
- objetos do editor de metadados, sobre
- metadados, objetos do editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640298"
---
# <a name="metadata-editor-object"></a>Objeto do editor de metadados

O objeto editor de metadados é usado para editar informações armazenadas na seção de cabeçalho de arquivos ASF. As coisas mais comuns manipuladas por esse objeto são atributos de metadados. Além disso, o editor de metadados lida com [*marcadores*](wmformat-glossary.md) e comandos de script. A única vez que você precisa usar o editor de metadados é quando deseja editar o cabeçalho de um arquivo existente sem reproduzi-lo.

O objeto editor de metadados é criado pela função [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), que define um ponteiro para uma interface **IWMMetadataEditor** . As outras interfaces do objeto editor de metadados podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto editor de metadados.



| Interface                                        | Descrição                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Permite a edição de aplicativos para examinar as propriedades de [*DRM*](wmformat-glossary.md) de um arquivo ASF sem ter nenhum direito para reproduzir o conteúdo protegido. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Manipula atributos, marcadores e comandos de script no cabeçalho.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Recupera informações de codec. Herda todos os métodos de **IWMHeaderInfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Fornece suporte avançado para atributos, incluindo atributos grandes, vários idiomas e nomes de atributos duplicados. Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Abre, fecha e salva as alterações no cabeçalho de um arquivo ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Abre um arquivo ASF para edição de cabeçalho com várias opções de compartilhamento e acesso a arquivos. Herda todos os métodos de **IWMMetadataEditor**.                                                              |



 

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

 

 




