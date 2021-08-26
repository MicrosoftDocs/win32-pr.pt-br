---
title: Trabalhando com metadados
description: Trabalhando com metadados
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows SDK de Formato de Mídia, visão geral de metadados
- AsF (Advanced Systems Format), visão geral dos metadados
- ASF (Formato de Sistemas Avançados), visão geral dos metadados
- metadados, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c001eed5330d3d90cdbf42cc52cfef3f048a25f7d8f72fe4402a48ccbb42480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109876"
---
# <a name="working-with-metadata"></a>Trabalhando com metadados

O suporte a metadados é fornecido pelo objeto writer, pelo leitor e pelos objetos de leitor síncronos e pelo objeto do editor de metadados. Para obter informações gerais sobre metadados, consulte [Metadados](metadata.md). Para obter informações sobre os recursos que suportam metadados no SDK Windows Media Format, consulte [Recursos de metadados](metadata-features.md).

A interface para edição de metadados é [**IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)que pode ser obtida chamando o **método QueryInterface** de qualquer interface em um dos objetos listados acima. **IWMHeaderInfo3** herda os métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2). Os métodos de **IWMHeaderInfo3** que lidam com atributos de metadados representam uma abordagem diferente para acessar metadados do que o usado pelos métodos **de IWMHeaderInfo**. Você sempre deve usar os métodos mais novos.

Os metadados em um arquivo ASF são identificados por um índice e um número de fluxo. Atributos de nível de arquivo são atribuídos a um número de fluxo de 0. Nas versões anteriores do SDK Windows Formato de Mídia, os atributos podiam ser identificados por nome. No entanto, como agora você pode duplicar nomes de atributo dentro de um fluxo, isso não é mais possível. Em vez disso, você pode recuperar todos os índices correspondentes a um nome. Para obter mais informações, consulte [Recuperando atributos de metadados](retrieving-metadata-attributes.md).

Para ajudar a localizar atributos rapidamente, você pode usar um número de fluxo especial, 0xFFFF. Use esse número de fluxo para identificar o arquivo como um todo, em vez de um fluxo específico ou os atributos de nível de arquivo. Os objetos do SDK Windows Formato de Mídia mantêm índices separados para cada fluxo e para os atributos de nível de arquivo. Ao usar fluxo 0xFFFF, os índices são diferentes daqueles que você usa ao especificar um fluxo específico. Por exemplo, o atributo que é o índice 0 para o fluxo 0 não será o mesmo que o atributo que é o índice 0 para fluxo 0xFFFF.

As seções a seguir descrevem o uso de metadados em mais detalhes.



| Seção                                                                    | Descrição                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Recuperando atributos de metadados](retrieving-metadata-attributes.md)       | Descreve como ler atributos de metadados de um header de arquivo.                     |
| [Definindo atributos de metadados](setting-metadata-attributes.md)             | Descreve como adicionar novos atributos de metadados a um header de arquivo.                    |
| [Editando atributos de metadados](editing-metadata-attributes.md)             | Descreve como editar atributos de metadados existentes.                               |
| [Removendo atributos de metadados](removing-metadata-attributes.md)           | Descreve como remover atributos de metadados existentes.                             |
| [Usando atributos de metadados complexos](using-complex-metadata-attributes.md) | Descreve como trabalhar com atributos cujos valores são representados por estruturas. |



 

Vários dos aplicativos de exemplo mostram como recuperar e editar metadados. Em particular, consulte o exemplo MetadataEdit, que vem nas versões C++ e C#.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> <dt>

[**Aplicativos de exemplo**](sample-applications.md)
</dt> </dl>

 

 




