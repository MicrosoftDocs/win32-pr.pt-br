---
description: A \_ tabela ForceCodepage é uma tabela especial usada para alterar a página de código de um pacote de instalação. Você pode determinar ou definir a página de código exportando ou importando um arquivo morto de texto chamado \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758318"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

A \_ tabela ForceCodepage é uma tabela especial usada para alterar a página de código de um pacote de instalação. Você pode determinar ou definir a página de código exportando ou importando um [arquivo morto de texto](text-archive-files.md) chamado \_ ForceCodepage. IDT.

O formato da \_ tabela ForceCodepage é 2 linhas em branco seguidas por uma terceira linha que indica a página de código numérico. Por exemplo, um \_ arquivo de tabela ForceCodepage. IDT para um banco de dados japonês seria semelhante ao seguinte. Nesse caso, a página de código numérico é 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Para obter mais informações sobre como usar \_ o ForceCodepage para obter ou definir a página de código de um banco de dados, consulte os tópicos a seguir.

-   [Manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md)
-   [Determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md)
-   [Configurando a página de código de um banco de dados](setting-the-code-page-of-a-database.md)

A \_ tabela ForceCodepage é uma pseudoclasse especial usada para alterar a página de código de um pacote de instalação. O uso da \_ tabela ForceCodepage define incondicionalmente o banco de dados para a página de código sem executar nenhuma validação para determinar se eles atualmente podem ser convertidos na nova página de código. É sempre recomendável que a alteração da página de código de um banco de dados seja iniciada com um banco de dados com neutralidade de idioma.

 

 



