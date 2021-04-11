---
title: Parâmetro MSWMExt (preterido)
description: Parâmetro MSWMExt (preterido)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Metaarquivos do Windows Media, parâmetro MSWMExt
- metaarquivos, parâmetro MSWMExt
- Parâmetro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365655"
---
# <a name="mswmext-parameter-deprecated"></a>Parâmetro MSWMExt (preterido)

O parâmetro *MSWMExt* indica para um programa cliente o formato de um arquivo referenciado.

**Sintaxe**


```XML

URL?MSWMExt=.
ext
```



**Código de exemplo**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>Comentários

Os programas cliente às vezes usam uma extensão de nome de arquivo ou um tipo MIME para determinar se um arquivo de mídia deve ser renderizado como um fluxo, renderizar o arquivo após um download completo ou se recusar a renderizar o arquivo. Se um programa cliente não puder determinar como tratar um arquivo de mídia com base na extensão de nome de arquivo ou no tipo MIME, ele poderá determinar como tratar o arquivo inspecionando o parâmetro *MSWMExt* . Por exemplo, o cliente poderia tratar o arquivo como se tivesse uma extensão igual ao valor do parâmetro *MSWMExt* . Para obter mais informações sobre tipos MIME e extensões de nome de arquivo, consulte [extensões de nome de arquivo](file-name-extensions.md). Para obter mais informações sobre o parâmetro *MSWMExt* , consulte o artigo [236895](https://support.microsoft.com/kb/236895) na base de dados de conhecimento Microsoft.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Versões anteriores de metaarquivos do Windows Media (preterido)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




