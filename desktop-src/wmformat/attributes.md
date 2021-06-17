---
title: Atributos (Windows Media Format 11 SDK)
description: Saiba mais sobre atributos no SDK do Windows Media Format 11. Um atributo é um item individual de metadados.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262188"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Atributos (Windows Media Format 11 SDK)

Um atributo é um item individual de metadados. A maioria dos atributos pode ser definida pelo seu aplicativo e gravada no cabeçalho de um arquivo ASF.

Alguns dos atributos predefinidos são atributos codificados. Esses atributos não são armazenados no cabeçalho de um arquivo ASF, mas são computados pelos objetos do Windows Media Format SDK quando o arquivo é carregado. Como os atributos codificados são sempre computados, eles são inerentemente somente leitura.

Esse SDK inclui muitas definições de atributo que você pode usar. Você também pode criar atributos próprios para descrever o conteúdo.

As seções a seguir descrevem os atributos predefinidos.



| Seção                                                                | Descrição                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lista de Atributos](attribute-list.md)                                   | Fornece uma lista alfabética de todos os atributos predefinidos. Após a lista, cada atributo é descrito individualmente.                                                                          |
| [Atributos com vários valores](attributes-with-multiple-values.md) | Lista os atributos que podem ser adicionados a um arquivo mais de uma vez.                                                                                                                                      |
| [Atributos por tipo](attributes-by-type.md)                           | Contém listas de atributos classificados por tipo. Isso inclui listas de atributos de finalidade especial (como aqueles que lidam com o gerenciamento de direitos digitais) e listas de atributos sugeridos por tipo de conteúdo. |
| [Suporte a marcas ID3](id3-tag-support.md)                                 | Lista os atributos que são compatíveis com marcas ID3.                                                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




