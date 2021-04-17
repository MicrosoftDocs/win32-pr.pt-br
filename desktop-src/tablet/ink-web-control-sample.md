---
description: Este exemplo mostra como criar um controle habilitado para tinta para uso em um navegador da Web. O exemplo usa o exemplo de formulário de declarações automáticas original e o transforma em um controle que é colocado em uma página da Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Exemplo de controle da Web de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761684"
---
# <a name="ink-web-control-sample"></a>Exemplo de controle da Web de tinta

Este exemplo mostra como criar um controle habilitado para tinta para uso em um navegador da Web. O exemplo usa o [exemplo de formulário de declarações automáticas](auto-claims-form-sample.md) original e o transforma em um controle que é colocado em uma página da Web.

Para obter mais informações sobre como usar a tinta na Web, consulte [tinta na Web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Modificações no projeto de exemplo original

Este exemplo consiste em uma solução que inclui dois projetos e um arquivo HTML. O primeiro projeto, autodeclarations, é um projeto de biblioteca de controle do Microsoft Visual C \# (um controle de usuário). O código-fonte para esse controle é quase idêntico ao da amostra de autodeclarações com duas diferenças:

-   A `AutoClaims` classe neste exemplo herda da classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) em vez da classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   A classe autodeclarations neste exemplo tem um método público adicionado, `DisposeResources` que descarta os controles filho internos usados para coletar tinta. Esse método deve ser chamado por thewebpageon que o controle é usado quando a página é concluída usando o controle.

## <a name="referencing-the-control-in-html"></a>Referenciando o controle em HTML

A solução inclui um arquivo HTML, default.htm. Esse arquivo é a página para a qual o navegador navega para carregar o controle. O arquivo contém uma <object> marca que faz referência ao controle. Ele também inclui um script que é chamado quando a página é descarregada, conforme indicado pela presença do atributo OnLoad = " `OnUnload()` " no <body> Tags. Essa função chama o `DisposeResources` método no controle para garantir que todos os recursos sejam liberados corretamente no desligamento.


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



Observe o formato do valor do atributo ClassID para a <object> marca. Ele nomeia o assembly, seguido de um \# separador de sinal e, em seguida, o namespace que contém o controle e, em seguida, o nome da classe do controle.

Um controle de usuário do mundo real provavelmente incluiria métodos adicionais usados para persistir ou enviar os dados coletados no aplicativo.

## <a name="the-autoclaims_webcontrol-project"></a>O projeto WebControl de autodeclaração \_

O projeto de WebControl de declarações autodeclaras \_ é um projeto de implantação que cria uma configuração que adiciona uma raiz virtual, o WebControl de autodeclaração \_ , no servidor Web quando instalado. O controle e o arquivo HTML são colocados nessa raiz virtual.

> [!Note]  
> Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK. Você deve concluir uma instalação personalizada e selecionar a subopção "amostras da Web pré-compiladas" para instalá-las.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de formulário de declarações automáticas](auto-claims-form-sample.md)
</dt> <dt>

[Tinta na Web](ink-on-the-web.md)
</dt> </dl>

 

 
