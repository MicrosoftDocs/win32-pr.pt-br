---
description: Demonstra como implementar um verbo shell usando o método CreateProcess.
title: Exemplo de verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858336"
---
# <a name="createprocess-verb-sample"></a>Exemplo de verbo CreateProcess

Demonstra como implementar um verbo shell usando o método CreateProcess.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="description"></a>Descrição

Os verbos baseados em CreateProcess dependem da execução de um executável e da passagem de um argumento de linha de comando. Esse método não é tão poderoso quanto os métodos DropTarget e ExecuteCommand, mas atinge o comportamento desejável fora do processo.

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

Para criar o exemplo no prompt de comando:

1.  Abra a janela do prompt de comando e navegue até **o diretório do projeto CreateProcessVerb.**
2.  Digite `msbuild CreateProcessVerb.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra Windows Explorer e navegue até o **diretório do projeto CreateProcessVerb.**
2.  Clique duas vezes no ícone do arquivo CreateProcessVerb.sln para abrir o projeto Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável usando o prompt de comando ou Windows Explorer.
2.  Na linha de comando, insira `CreateProcessVerb.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para CreateProcessVerb.exe.
3.  Siga as instruções na caixa de diálogo exibida

 

 



