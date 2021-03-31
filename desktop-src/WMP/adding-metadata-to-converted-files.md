---
title: Adicionando metadados a arquivos convertidos
description: Adicionando metadados a arquivos convertidos
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, processo de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, adicionando metadados a arquivos convertidos
- adicionando metadados a arquivos convertidos
- metadados, adicionando aos arquivos convertidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641208"
---
# <a name="adding-metadata-to-converted-files"></a>Adicionando metadados a arquivos convertidos

Os arquivos convertidos devem conter determinados metadados para garantir uma boa experiência do usuário. No mínimo, os arquivos convertidos devem conter os atributos principais listados nas [diretrizes de uso de metadados do Windows Media](/previous-versions/ms867702(v=msdn.10)).

Para arquivos de música, defina o valor de **WM/MediaClassPrimaryID** como D1607DBC-E323-4BE2-86A1-48A42A28441E.

Para arquivos de caixa postal, defina o valor de **WM/MediaClassPrimaryID** como 01CD0F29-DA4E-4157-897B-6275D50C4F11, que é o GUID de classe primária para arquivos de áudio. Defina o valor de **WM/MediaClassSecondaryID** como 193c8824-4d52-4178-90bd-305240b04636.

Para notas de voz, defina o valor de **WM/MediaClassPrimaryID** como 01CD0F29-DA4E-4157-897B-6275D50C4F11. Defina o valor de **WM/MediaClassSecondaryID** como 3A172A13-2BD9-4831-835B-114F6A95943F.

Defina o valor de **WM/ContentDistributor** como o nome da chave para o serviço de música que forneceu o conteúdo.

Defina o valor de **WM/UniqueFileIdentifier** como a ID de conteúdo. Isso permitirá que você recupere itens de conteúdo específicos em um momento futuro.

Defina um valor para o **WM/WMShadowFileSourceFileType**.

Para conteúdo protegido, use o SDK do Windows Media Format para definir o atributo **DRM \_ DRMHeader \_ ContentId** como a ID do conteúdo.

Para conteúdo protegido, defina um valor para **WM/WMShadowFileSourceDRMType**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre plug-ins de conversão**](about-conversion-plug-ins.md)
</dt> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 