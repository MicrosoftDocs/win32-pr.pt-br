---
description: Demonstra como escrever um manipulador usado para exibir uma visualização de arquivo dentro do painel de visualização do Windows Explorer ou outros hosts do Gerenciador de visualização.
title: Exemplo do manipulador de visualização de receitas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968074"
---
# <a name="recipe-preview-handler-sample"></a>Exemplo do manipulador de visualização de receitas

Demonstra como escrever um manipulador usado para exibir uma visualização de arquivo dentro do painel de visualização do Windows Explorer ou outros hosts do Gerenciador de visualização.

Este tópico contém as seguintes seções:

-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Cancelando o registro da DLL do Gerenciador de visualização de exemplo](#unregistering-the-sample-preview-handler-dll)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de RecipePreviewHandler](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **RecipePreviewHandler** . Por exemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.
2.  Digite `msbuild PreviewHandlerSDKSample.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **RecipePreviewHandler** .
2.  Clique duas vezes no ícone do arquivo PreviewHandlerSDKSample. sln para abrir o projeto no Visual Studio.
    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar** , selecione **Compilar solução**.

> [!Note]  
> Se o sistema de destino for de 64 bits (x64), esse Gerenciador de visualização de exemplo deve ser criado como um aplicativo de 64 bits.

 

## <a name="running-the-sample"></a>Executando o exemplo

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **RecipePreviewHandler** criado. Por exemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`. Insira `regsvr32.exe PreviewHandlerSDKSample.dll` para registrar o manipulador.
2.  Abra o Windows Explorer e mostre o painel de visualização se ele ainda não estiver sendo exibido.
    -   **Windows 7**: clique no botão painel de visualização.
    -   **Windows Vista**: clique no menu **organizar** , vá para o submenu **layout** e selecione **painel de visualização**.
3.  Use o Windows Explorer para navegar até o diretório do projeto **RecipePreviewHandler** .
4.  Selecione o arquivo. recipe de exemplo.

Para fazer com que a saída de 32 bits (x86) e 64 bits (x64) funcione em uma versão de 64 bits do Windows, defina o valor **AppID** para o host substituto do WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , conforme mostrado no código a seguir.


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>Cancelando o registro da DLL do Gerenciador de visualização de exemplo

-   Abra a janela de prompt de comando e insira `regsvr32.exe /u PreviewHandlerSDKSample.dll` para cancelar o registro do manipulador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
