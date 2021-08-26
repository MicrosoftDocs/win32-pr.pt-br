---
description: A \_ tabela ForceCodepage é uma tabela especial usada para alterar a página de código de um pacote de instalação. Você pode determinar ou definir a página de código exportando ou importando um arquivo de arquivo de texto chamado \_ ForceCodepage.idt.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee252260b0aaee9713c28af5a6d810a3f6a8ed1c1b376b52bd82472cebfd0853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979596"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

A \_ tabela ForceCodepage é uma tabela especial usada para alterar a página de código de um pacote de instalação. Você pode determinar ou definir [a](text-archive-files.md) página de código exportando ou importando um arquivo de arquivo de texto chamado \_ ForceCodepage.idt.

O formato da tabela ForceCodepage é de duas linhas em branco seguidas por uma terceira linha que \_ indica a página de código numérico. Por exemplo, um arquivo .idt da tabela ForceCodepage para um banco de dados \_ japonês teria a aparência a seguir. A página de código numérico nesse caso é 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Para obter mais informações sobre como usar ForceCodepage para obter ou definir a página de código de um banco de \_ dados, consulte os tópicos a seguir.

-   [Manipulação de página de código (Windows instalador)](code-page-handling-windows-installer-.md)
-   [Determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md)
-   [Definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md)

A \_ tabela ForceCodepage é uma pseudo tabela especial usada para alterar a página de código de um pacote de instalação. Usar a tabela ForceCodepage define incondicionalmente o banco de dados para a página de código sem executar nenhuma validação sobre se os dados atualmente no banco de dados podem ser convertidos para a nova \_ página de código. É sempre recomendável que a alteração da página de código de um banco de dados comece com um banco de dados neutro em idioma.

 

 



