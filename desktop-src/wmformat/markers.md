---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows SDK do formato de mídia, marcadores
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- marcadores, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58ddc013b2d8e09fa30ac6a8b7373aaf6733b669f2ccacec6350ee70e0800b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808226"
---
# <a name="markers"></a>Marcadores

Os marcadores são chamados de locais na linha do tempo de um arquivo ASF. Cada marcador tem um nome e um tempo de apresentação que você atribui. Você pode especificar quantos marcadores forem necessários para um arquivo.

Os marcadores são úteis para dividir arquivos ASF grandes em partes lógicas. Um aplicativo que usa o objeto leitor para reproduzir arquivos ASF pode fornecer ao usuário a opção de ignorar o marcador para o marcador, simplificando a navegação da mídia digital. Por exemplo, se você estiver fazendo um arquivo ASF de uma apresentação, poderá colocar marcadores na linha do tempo para cada tópico principal que é discutido. Na reprodução, em vez de obter uma linha do tempo longa e ter de adivinhar no local para o qual buscar, um usuário pode simplesmente escolher um tópico de uma lista e ir direto para a parte pertinente do arquivo.

Os marcadores são manipulados pelo objeto editor de metadados. Você pode adicionar, remover e exibir os marcadores em um arquivo a qualquer momento depois que o arquivo tiver sido gravado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Para buscar marcadores**](to-seek-to-markers.md)
</dt> <dt>

[**Usando marcadores**](using-markers.md)
</dt> </dl>

 

 




