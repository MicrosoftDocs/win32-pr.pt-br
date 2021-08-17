---
title: Instalando enquanto estiver offline
description: Instalando enquanto estiver offline
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player lojas online, instalando enquanto estiver offline
- lojas online, instalando enquanto estiver offline
- Digite 1 lojas online, instalando enquanto estiver offline
- Digite 2 lojas online, instalando enquanto estiver offline
- Windows Media Player lojas online, instalações offline
- lojas online, instalações offline
- tipos 1 lojas online, instalações offline
- tipo 2 lojas online, instalações offline
- Instalando lojas online offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3051aca9634bc2c53950baa783bcf62fc6861c616facd9dc563d70d011c2459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135499"
---
# <a name="installing-while-offline"></a>Instalando enquanto estiver offline

os usuários podem instalar o Windows Media Player enquanto não estão conectados à Internet. quando isso acontece, Windows Media Player a instalação localiza o documento ServiceInfo.xml especificado pelo parâmetro de linha de comando *serviceinfo* . Se o atributo de **chave** corresponder ao parâmetro de linha de comando *defaultservice* , a instalação aplicará informações dos seguintes elementos a Windows Media Player:

-   FriendlyName. o nome amigável do repositório online é mostrado na interface do usuário do Windows Media Player.
-   Cor. As cores especificadas são aplicadas à barra de tarefas e aos botões.
-   ServiceTask1, ServiceTask2 e ServiceTask3. Os elementos filho ButtonText e ButtonTip são definidos. O atributo de URL não está definido. a URL é definida quando o usuário se conecta à Internet e Windows Media Player recupera sua lista de lojas online da maneira normal.
-   Imagem. Os atributos MenuURL e ServiceLargeURL estão definidos. Essas URLs devem apontar para as imagens que você instalou no disco rígido do usuário usando o protocolo file://.

quando o usuário tenta exibir a loja online, Windows Media Player exibe uma mensagem informando ao usuário que uma conexão com a Internet é necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento Color**](color-element.md)
</dt> <dt>

[**Elemento FriendlyName**](friendlyname-element.md)
</dt> <dt>

[**Elemento Image**](image-element.md)
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

 

 




