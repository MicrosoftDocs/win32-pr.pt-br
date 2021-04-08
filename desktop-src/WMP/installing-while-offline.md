---
title: Instalando enquanto estiver offline
description: Instalando enquanto estiver offline
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Armazenamentos online do Windows Media Player, instalando enquanto estiver offline
- lojas online, instalando enquanto estiver offline
- Digite 1 lojas online, instalando enquanto estiver offline
- Digite 2 lojas online, instalando enquanto estiver offline
- Lojas online do Windows Media Player, instalações offline
- lojas online, instalações offline
- tipos 1 lojas online, instalações offline
- tipo 2 lojas online, instalações offline
- Instalando lojas online offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822742"
---
# <a name="installing-while-offline"></a>Instalando enquanto estiver offline

Os usuários podem instalar o Windows Media Player enquanto não estiverem conectados à Internet. Quando isso acontece, a instalação do Windows Media Player localiza o ServiceInfo.xml documento especificado pelo parâmetro de linha de comando *serviceInfo* . Se o atributo de **chave** corresponder ao parâmetro de linha de comando *defaultservice* , a instalação aplicará informações dos seguintes elementos ao Windows Media Player:

-   FriendlyName. O nome amigável da loja online é mostrado na interface do usuário do Windows Media Player.
-   Cor. As cores especificadas são aplicadas à barra de tarefas e aos botões.
-   ServiceTask1, ServiceTask2 e ServiceTask3. Os elementos filho ButtonText e ButtonTip são definidos. O atributo de URL não está definido. A URL é definida quando o usuário se conecta à Internet e o Windows Media Player recupera sua lista de lojas online da maneira normal.
-   Imagem. Os atributos MenuURL e ServiceLargeURL estão definidos. Essas URLs devem apontar para as imagens que você instalou no disco rígido do usuário usando o protocolo file://.

Quando o usuário tenta exibir a loja online, o Windows Media Player exibe uma mensagem informando ao usuário que uma conexão com a Internet é necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento Color**](color-element.md)
</dt> <dt>

[**Elemento FriendlyName**](friendlyname-element.md)
</dt> <dt>

[**Elemento de imagem**](image-element.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento serviceInfo**](serviceinfo-element.md)
</dt> <dt>

[**Elemento ServiceTask1**](servicetask1-element.md)
</dt> <dt>

[**Elemento ServiceTask2**](servicetask2-element.md)
</dt> <dt>

[**Elemento ServiceTask3**](servicetask3-element.md)
</dt> <dt>

[**Configurando a loja online inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Parâmetros de linha de comando de instalação para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




