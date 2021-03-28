---
description: Demonstra como implementar um verbo do shell usando o método CreateProcess.
title: Exemplo de verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968095"
---
# <a name="createprocess-verb-sample"></a>Exemplo de verbo CreateProcess

Demonstra como implementar um verbo do shell usando o método CreateProcess.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="description"></a>Description

Os verbos baseados em CreateProcess dependem da execução de um executável e da passagem de um argumento de linha de comando. Esse método não é tão potente quanto os métodos DropTarget e ExecuteCommand, mas alcança o comportamento de fora do processo desejado.

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de CreateProcessVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **CreateProcessVerb** .
2.  Digite `msbuild CreateProcessVerb.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **CreateProcessVerb** .
2.  Clique duas vezes no ícone do arquivo CreateProcessVerb. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Na linha de comando, digite `CreateProcessVerb.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para CreateProcessVerb.exe.
3.  Siga as instruções na caixa de diálogo exibida

 

 



