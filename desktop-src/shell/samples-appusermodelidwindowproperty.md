---
description: Demonstra como controlar o comportamento de agrupamento da barra de tarefas de janelas de um aplicativo por meio da propriedade System.AppUserModel.ID.
title: Exemplo da propriedade janela de ID do modelo do usuário do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a6a4b0daca8b6bd4147c1e36d921b58b3802d975e678e49a9b9153761e61820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219876"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Exemplo da propriedade da janela de ID do modelo de usuário do aplicativo (AppID)

Demonstra como controlar o comportamento de agrupamento da barra de tarefas de janelas de um aplicativo por meio da propriedade [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo mostra como definir a propriedade [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) por meio do uso da implementação de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) da janela, que é obtida por meio de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Location      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de AppUserModelIDWindowProperty](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **AppUserModelIDWindowProperty** .
2.  Insira `msbuild AppUserModelIDWindowProperty.sln`.

para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  abra Windows Explorer e navegue até o diretório do projeto **AppUserModelIDWindowProperty** .
2.  Clique duas vezes no ícone do arquivo AppUserModelIDWindowProperty. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  navegue até o diretório que contém o novo executável, usando o prompt de comando ou o gerenciador de Windows.
2.  Na linha de comando, digite `AppUserModelIDWindowProperty.exe` . como alternativa, no Windows Explorer, clique duas vezes no ícone para AppUserModelIDWindowProperty.exe.
3.  Para demonstrar o efeito que as IDs de modelo de usuário do aplicativo (AppUserModelIDs) têm no agrupamento da barra de tarefas, inicie pelo menos três instâncias do aplicativo ao mesmo tempo.
4.  Use o menu para definir um AppUserModelID diferente em cada uma das três janelas. Observe que cada AppUserModelID separado resulta em um botão de barra de tarefas separado e que o Windows pode alterar sua identidade em tempo de execução.
5.  Defina pelo menos duas janelas para o segundo AppUserModelID. Observe que ambos se movem para o mesmo grupo da barra de tarefas.
6.  Abra a **barra de tarefas e a janela Propriedades do menu iniciar** clicando com o botão direito do mouse na barra de tarefas e selecionando **Propriedades** no menu de contexto. Altere os **botões da barra de tarefas:** lista suspensa entre **combinar quando a barra de tarefas estiver cheia** e **nunca combinar** valores. Observe que cada janela pode obter um botão separado, mas que os botões são agrupados por AppUserModelID.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
