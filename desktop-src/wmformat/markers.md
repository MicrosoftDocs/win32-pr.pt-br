---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marcadores
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- marcadores, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823006"
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

 

 




