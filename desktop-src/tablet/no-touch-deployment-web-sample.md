---
description: Este exemplo mostra como implantar um aplicativo gerenciado do Tablet PC pela Web usando a implantação no-touch.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Exemplo de Web de implantação No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104506324"
---
# <a name="no-touch-deployment-web-sample"></a>Exemplo de Web de implantação No-Touch

Este exemplo mostra como implantar um aplicativo gerenciado do Tablet PC pela Web usando a implantação no-touch. Você deve estar familiarizado com os conceitos discutidos em [implantação sem interatividade no .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp). Seu computador deve ter o Microsoft Serviços de Informações da Internet (IIS) instalado para executar este exemplo.

## <a name="overview"></a>Visão geral

Com a implantação do-touch, aplicativos do Tablet PCWindows Forms-aplicativos da área de trabalho criados usando as classes no namespace System. Windows. Forms do Microsoft .NET Framework e o Microsoft Windows XP Tablet PC Edition Development Kit 1,7-podem ser baixados, instalados e executados diretamente nos computadores dos usuários sem qualquer alteração do registro ou componentes do sistema compartilhado.

Este exemplo usa o projeto original para [exemplo de formulário de declarações automática](auto-claims-form-sample.md), autodeclaras e fornece um projeto de instalador, autodeclaras \_ NoTouchWeb. Depois de compilado e executado, o projeto do instalador cria uma nova raiz virtual, também chamada de autodeclaração \_ NoTouchWeb. O instalador copia um arquivo, default.htm, que inclui um link para o assembly AutoClaims.exe. Para iniciar o aplicativo cliente avançado, navegue até a raiz virtual com o Microsoft Internet Explorer e, em seguida, clique no link na página default.htm.

> [!Note]  
> Você deve navegar até a raiz virtual por meio do IIS (por exemplo, https://localhost/AutoClaims\_NoTouchWeb/default.htm) e não diretamente por meio do sistema de arquivos para que o aplicativo funcione no domínio do aplicativo Internet Explorer.

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a>Requisitos de implantação do No-Touch

Todos os assemblies dependentes devem estar localizados no caminho de pesquisa do assembly ou na raiz do diretório virtual do site. O projeto de implantação NoTouchWeb de autodeclarações \_ instala o assembly e a página de referência, default.htm, na mesma raiz virtual (autodeclarações \_ NoTouchWeb).

> [!Note]  
> Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK. Você deve concluir uma instalação personalizada e selecionar a subopção "amostras da Web pré-compiladas" para instalá-las.

 

Para obter mais informações sobre como usar a tinta na Web, consulte [tinta na Web](ink-on-the-web.md).

 

 