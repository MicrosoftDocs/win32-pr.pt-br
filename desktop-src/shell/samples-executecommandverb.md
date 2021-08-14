---
description: Demonstra como implementar um verbo do shell usando o método ExecuteCommand.
title: Exemplo do verbo de comando executar
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e32b472d63b9d2d779c97b64833f354e7d4d2eaed034d3a213ae4e101f7beb3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858265"
---
# <a name="execute-command-verb-sample"></a>Exemplo do verbo de comando executar

Demonstra como implementar um verbo do shell usando o método ExecuteCommand.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="description"></a>Descrição

Esse método é preferido para implementações de verbo, pois fornece mais flexibilidade, é simples e dá suporte à ativação fora do processo. Este exemplo implementa um objeto COM (servidor local Component Object Model) autônomo, mas é esperado que a implementação do verbo seja integrada aos aplicativos existentes. Para fazer isso, seu objeto de aplicativo principal deve registrar uma fábrica de classes para si mesmo. Esse objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para verbos do seu aplicativo. Observe que COM inicia seu aplicativo se ele ainda não estiver em execução, mas se conectará a uma instância em execução do seu aplicativo, se houver um.

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de ExecuteCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **ExecuteCommandVerb** .
2.  Digite `msbuild ExecuteCommand.sln`.

para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  abra Windows Explorer e navegue até o diretório do projeto **ExecuteCommandVerb** .
2.  Clique duas vezes no ícone do arquivo ExecuteCommand. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  navegue até o diretório que contém o novo executável, usando o prompt de comando ou o gerenciador de Windows.
2.  Na linha de comando, digite `ExecuteCommand.exe` . como alternativa, no Windows Explorer, clique duas vezes no ícone para ExecuteCommand.exe.
3.  Siga as instruções na caixa de diálogo exibida

 

 
