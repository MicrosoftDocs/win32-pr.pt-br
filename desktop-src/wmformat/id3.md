---
title: Suporte a ID3
description: ID3 é uma organização que definiu um conjunto de padrões para incluir metadados em arquivos de áudio MPEG (camada 3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows SDK do formato de mídia, suporte a ID3
- ASF (Advanced Systems Format), suporte a ID3
- ASF (formato de sistemas avançados), suporte a ID3
- metadados, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c92fb9282483b6fd01b1149220e5f30421c3c1285bd533d64afef91709314e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702977"
---
# <a name="id3-support"></a>Suporte a ID3

ID3 é uma organização que definiu um conjunto de padrões para incluir metadados em arquivos de áudio MPEG (camada 3). os objetos do SDK do formato de mídia Windows fornecem suporte para atributos compatíveis ID3. Há suporte para três versões de ID3 distintas: ID3v1. x, ID3v 2.2 e ID3v 2.3/v2, 4. Para obter uma lista dos atributos que correspondem a quadros ID3, consulte [suporte a marcas ID3](id3-tag-support.md).

Salvo indicação em contrário, nenhuma validação dos dados de quadro ID3 é executada pelos objetos deste SDK. Por exemplo, o atributo de metadados [**WM/música \_ sincronizado**](wm-lyrics-synchronised.md) armazena as músicas de música com carimbos de data/hora correspondentes. Ao gravar um atributo **\_ sincronizado do WM/música** , os objetos desse SDK não verificarão se os carimbos de data/hora estão em ordem cronológica ou realizam a validação de qualquer tipo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Recursos de metadados**](metadata-features.md)
</dt> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




