---
description: Este exemplo mostra como implantar um aplicativo de tablet gerenciado pela Web usando a implantação sem toque.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch web de implantação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d8fb9989785dc081022c2e76d8fade6d48bf521b3f27449ff5aac963706f356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449647"
---
# <a name="no-touch-deployment-web-sample"></a>No-Touch web de implantação de dados

Este exemplo mostra como implantar um aplicativo de tablet gerenciado pela Web usando a implantação sem toque. Você deve estar familiarizado com os conceitos discutidos em [Implantação](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)sem toque no .NET Framework . Seu computador deve ter Serviços de Informações da Internet da Microsoft (IIS) instalado para executar este exemplo.

## <a name="overview"></a>Visão geral

Com a implantação sem toque, o Tablet PCWindows Forms aplica aplicativos da área de trabalho criado usando as classes no Sistema. Windows. O namespace de formulários do Microsoft .NET Framework e do Microsoft Windows XP Tablet PC Edition Development Kit 1.7 pode ser baixado, instalado e executado diretamente nos computadores dos usuários sem nenhuma alteração do Registro ou dos componentes do sistema compartilhado.

Este exemplo leva o projeto original para [Exemplo](auto-claims-form-sample.md)de Formulário de Declarações Automáticas, AutoClaims e fornece um projeto do instalador, AutoClaims \_ NoTouchWeb. Depois de compilado e executado, o projeto do instalador cria uma nova raiz virtual, também chamada AutoClaims \_ NoTouchWeb. O instalador copia um arquivo, default.htm, que inclui um link para o assembly AutoClaims.exe. Para iniciar o aplicativo cliente rico, navegue até a raiz virtual com o Microsoft Internet Explorer e clique no link na página default.htm aplicativo.

> [!Note]  
> Você deve navegar até a raiz virtual por meio do IIS (por exemplo, e não diretamente pelo sistema de arquivos para que o aplicativo funcione no domínio Internet Explorer https://localhost/AutoClaims\_NoTouchWeb/default.htm) aplicativo.

 


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



## <a name="no-touch-deployment-requirements"></a>No-Touch de implantação

Todos os assemblies dependentes devem estar localizados no caminho de pesquisa do assembly ou na raiz do diretório virtual do site. O projeto de implantação AutoClaims NoTouchWeb instala o assembly e a página de referência, default.htm, na mesma \_ raiz virtual (AutoClaims \_ NoTouchWeb).

> [!Note]  
> Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK. Você deve concluir uma instalação personalizada e selecionar a sub-opção "Exemplos da Web pré-compilados" para instalá-los.

 

Para obter mais informações sobre como usar tinta na Web, consulte [Ink na Web.](ink-on-the-web.md)

 

 