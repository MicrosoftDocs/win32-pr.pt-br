---
title: Arquitetura do Gerenciador de download
description: Arquitetura do Gerenciador de download
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- arquitetura do Gerenciador de download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635255"
---
# <a name="download-manager-architecture"></a>Arquitetura do Gerenciador de download

O Gerenciador de download do Windows Media Player usa a tecnologia COM. A funcionalidade é ditáticas em um conjunto de interfaces de programação; Você pode escrever o código de programação que usa essas interfaces usando o Microsoft JScript ou o C++.

As linguagens de script usam o conceito de objetos para dividir a funcionalidade de programação. O modelo de objeto **DownloadManager** usa vários objetos para dividir os métodos e as propriedades em uma organização lógica que agrupa funções semanticamente relacionadas. As seções a seguir contêm informações sobre os objetos do Gerenciador de download.



| Seção                                                                     | Descrição                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Sobre o objeto DownloadManager](#about-the-downloadmanager-object)       | O objeto **DownloadManager** representa o objeto raiz do Gerenciador de download do Windows Media Player. |
| [Sobre o objeto Downloadcollection](#about-the-downloadcollection-object) | O objeto **downloadcollection** representa uma coleção de itens de download.                             |
| [Sobre o objeto DownloadItem](#about-the-downloaditem-object)             | O objeto **DownloadItem** representa uma solicitação de download individual.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Sobre o objeto DownloadManager

**DownloadManager** é o objeto raiz do Gerenciador de download do Windows Media Player. Todos os outros objetos são acessados por esse objeto. Para obter acesso ao objeto **DownloadManager** , use a seguinte sintaxe do JScript:


```C++
var DownloadManager = external.DownloadManager;
```



Isso cria uma instância do objeto **DownloadManager** , que pode ser usada para recuperar os objetos filho. Por exemplo, a sintaxe a seguir recupera o primeiro item da coleção de download com o número de ID 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Sobre o objeto Downloadcollection

O objeto **downloadcollection** representa uma coleção de arquivos a serem baixados. Você pode usar esse objeto para determinar quantos downloads estão na coleção, remover itens da coleção, recuperar um item de download específico e iniciar um novo download. Iniciar um novo download adiciona automaticamente o download à coleção.

## <a name="about-the-downloaditem-object"></a>Sobre o objeto DownloadItem

O objeto **DownloadItem** representa um download individual. Os itens de download sempre existem como parte de uma coleção de download. Use esse objeto para recuperar informações sobre o item de download e para pausar, retomar ou cancelar o download em andamento.

Quando você cancela um download, o item de download permanece em vigor em sua coleção de download. Nesse caso, **downloadcollection**. **downloadstate** recupera um valor de 4, significando cancelado.

Você pode usar **downloadItem**. **progresso** para informar ao usuário sobre quanto do arquivo foi transferido ou quanto resta ser baixado. Você pode usar esse valor para estimar o tempo restante também.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciador de download**](download-manager.md)
</dt> </dl>

 

 




