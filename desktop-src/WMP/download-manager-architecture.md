---
title: Arquitetura do Gerenciador de Download
description: Arquitetura do Gerenciador de Download
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player online, Gerenciador de Download
- lojas online, Gerenciador de Download
- tipo 2 lojas online, Gerenciador de Download
- Windows Media Player, Gerenciador de Download
- Windows Media Player Gerenciador de Download
- Gerenciador de Download
- arquitetura do Gerenciador de Download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae04be86d935f87202abe4b0bf73e833a9da07cf89526b9dcb60de31eb881a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997096"
---
# <a name="download-manager-architecture"></a>Arquitetura do Gerenciador de Download

O Windows Media Player Download Manager usa a tecnologia COM. A funcionalidade é desenvolvida em um conjunto de interfaces de programação; você pode escrever código de programação que usa essas interfaces usando o Microsoft JScript ou C++.

As linguagens de script usam o conceito de objetos para dividir a funcionalidade de programação. O **modelo de objeto DownloadManager** usa vários objetos para dividir os métodos e as propriedades em uma organização lógica que reúne funções semanticamente relacionadas. As seções a seguir contêm informações sobre os objetos do Gerenciador de Download.



| Seção                                                                     | Descrição                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Sobre o objeto DownloadManager](#about-the-downloadmanager-object)       | O **objeto DownloadManager** representa o objeto raiz do Windows Media Player Download Manager. |
| [Sobre o objeto DownloadCollection](#about-the-downloadcollection-object) | O **objeto DownloadCollection** representa uma coleção de itens de download.                             |
| [Sobre o objeto DownloadItem](#about-the-downloaditem-object)             | O **objeto DownloadItem** representa uma solicitação de download individual.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Sobre o objeto DownloadManager

**DownloadManager** é o objeto raiz do gerenciador Windows Media Player Download. Todos os outros objetos são acessados por meio desse objeto . Para obter acesso ao **objeto DownloadManager,** use a seguinte sintaxe JScript:


```C++
var DownloadManager = external.DownloadManager;
```



Isso cria uma instância do **objeto DownloadManager,** que pode ser usada para recuperar os objetos filho. Por exemplo, a sintaxe a seguir recupera o primeiro item da coleção de download que tem o número de ID 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Sobre o objeto DownloadCollection

O **objeto DownloadCollection** representa uma coleção de arquivos a serem baixados. Você pode usar esse objeto para determinar quantos downloads estão na coleção, remover itens da coleção, recuperar um item de download específico e iniciar um novo download. Iniciar um novo download adiciona automaticamente o download à coleção.

## <a name="about-the-downloaditem-object"></a>Sobre o objeto DownloadItem

O **objeto DownloadItem** representa um download individual. Itens de download sempre existem como parte de uma coleção de download. Use esse objeto para recuperar informações sobre o item de download e pausar, retomar ou cancelar o download em andamento.

Quando você cancela um download, o item de download permanece em seu conjunto de downloads. Nesse caso, **baixeCollection**. **downloadState** recupera um valor de 4, o que significa cancelado.

Você pode usar **downloadItem**. **para** informar o usuário sobre quanto do arquivo foi transferido ou quanto ainda deve ser baixado. Você também pode usar esse valor para estimar o tempo restante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciador de Download**](download-manager.md)
</dt> </dl>

 

 




