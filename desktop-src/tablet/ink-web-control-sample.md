---
description: Este exemplo mostra como criar um controle habilitado para tinta para uso em um navegador da Web. O exemplo pega o Exemplo de Formulário de Declarações Automáticas original e o transforma em um controle que é colocado em uma página da Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Exemplo de controle da Web de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a2f305f1dcbb412325970510c6eaa5f09732bf10d870c961820ab8d8749eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032194"
---
# <a name="ink-web-control-sample"></a>Exemplo de controle da Web de tinta

Este exemplo mostra como criar um controle habilitado para tinta para uso em um navegador da Web. O exemplo pega o Exemplo [de Formulário de Declarações](auto-claims-form-sample.md) Automáticas original e o transforma em um controle que é colocado em uma página da Web.

Para obter mais informações sobre como usar tinta na Web, consulte [Ink na Web.](ink-on-the-web.md)

## <a name="modifications-to-the-original-sample-project"></a>Modificações na amostra original Project

Este exemplo consiste em uma solução que inclui dois projetos e um arquivo HTML. O primeiro projeto, AutoClaims, é um projeto da Biblioteca de Controles do Microsoft Visual C \# (um Controle de Usuário). O código-fonte desse controle é quase idêntico ao da amostra AutoClaims com duas diferenças:

-   A `AutoClaims` classe neste exemplo herda da classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) em vez da [classe](/dotnet/api/system.windows.forms.form?view=netcore-3.1) Form.

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   A Classe AutoClaims neste exemplo tem um método público adicionado, que descarta os controles filho internos usados `DisposeResources` para coletar tinta. Esse método deve ser chamado pelawebpageon em que o controle é usado quando essa página é concluída usando o controle .

## <a name="referencing-the-control-in-html"></a>Referenciando o controle em HTML

A solução inclui um arquivo HTML, default.htm. Esse arquivo é a página para a que o navegador navega para carregar o controle. O arquivo contém uma <object> marca que faz referência ao controle . Ele também inclui um script que é chamado quando a página é descarregada, conforme indicado pela presença do atributo onload=" `OnUnload()` no <body> tag. Essa função chama o `DisposeResources` método no controle para garantir que todos os recursos sejam liberados corretamente no desligamento.


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



Observe o formato do valor do atributo classid para a <object> marca. Ele nomeia o assembly, seguido por um separador de sinal e, em seguida, o namespace que contém o controle e, em seguida, o nome \# de classe do controle.

Um controle de usuário do mundo real provavelmente incluiria métodos adicionais usados para persistir ou enviar os dados coletados no aplicativo.

## <a name="the-autoclaims_webcontrol-project"></a>O controle \_ WebControl autoClaims Project

O projeto AutoClaims WebControl é uma implantação Project que cria uma configuração que adiciona uma raiz \_ virtual, AutoClaims WebControl, ao servidor Web quando \_ instalado. O controle e o arquivo HTML são colocados nessa raiz virtual.

> [!Note]  
> Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK. Você deve concluir uma instalação personalizada e selecionar a sub-opção "Exemplos da Web pré-compilados" para instalá-los.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de formulário de declarações automáticas](auto-claims-form-sample.md)
</dt> <dt>

[Tinta na Web](ink-on-the-web.md)
</dt> </dl>

 

 
