---
title: Objeto DownloadManager
description: Objeto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player online, objeto DownloadManager
- online stores,objeto DownloadManager
- tipo 2 lojas online, objeto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 500061e414d7321ed6fe4c46cafc79cd6795935847bb3d8c527364497722ecf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340520"
---
# <a name="downloadmanager-object"></a>Objeto DownloadManager

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **objeto DownloadManager** é o objeto raiz do Windows Media Player Download Manager. Ele pode ser usado por páginas da Web hospedadas em painéis de tarefas do serviço de loja online.

O **objeto DownloadManager** dá suporte aos métodos a seguir.



| Método                                                                   | Descrição                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Cria uma coleção de download vazia.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Recupera a coleção de download especificada. |



 

O **objeto DownloadManager** é acessado usando **externo. DownloadManager**. Para fins de ilustração, supõe-se que esse valor tenha sido atribuído a uma variável chamada "DownloadManager", que será usada para identificar esse objeto nas seções de sintaxe de referência.

No Windows Media Player 10 ou posterior, a propriedade e o objeto **DownloadManager** só podem ser acessados nos painéis de tarefas do serviço de loja online. Não é possível usar **o DownloadManager** de outros recursos em que o objeto Externo está disponível, como HTMLView, Exibição do Info Center e informações do álbum. 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




