---
description: Demonstra como implementar um verbo do shell usando o método DropTarget.
title: Exemplo de verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967996"
---
# <a name="droptarget-verb-sample"></a>Exemplo de verbo DropTarget

Demonstra como implementar um verbo do shell usando o método DropTarget.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="description"></a>Description

Este exemplo mostra como implementar um verbo do shell usando o método DropTarget. Esse método é preferido para implementações de verbo que devem funcionar no Windows XP. Este exemplo implementa um objeto COM (servidor local Component Object Model) autônomo, mas espera-se que a implementação do verbo seja integrada aos aplicativos existentes. Para fazer isso, o objeto de aplicativo principal registra uma fábrica de classes para si mesmo. Esse objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para verbos do seu aplicativo. Observe que COM inicia seu aplicativo se ele ainda não estiver em execução, mas se conectará a uma instância em execução do seu aplicativo, se houver um.

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de DropTargetVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **DropTargetVerb** .
2.  Digite `msbuild DropTargetVerb.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **DropTargetVerb** .
2.  Clique duas vezes no ícone do arquivo DropTargetVerb. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Na linha de comando, digite `DropTargetVerb.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para DropTargetVerb.exe.
3.  Siga as instruções na caixa de diálogo exibida

 

 
