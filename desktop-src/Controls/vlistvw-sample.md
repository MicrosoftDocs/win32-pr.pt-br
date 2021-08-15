---
title: Exemplo de VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Saiba mais sobre: exemplo de VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefcd39c44e79ab4eec23f7becf202d1a3cd3566f6be9496e9fd61b577c87f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957555"
---
# <a name="vlistvw-sample"></a>Exemplo de VListVW

Este tópico descreve o exemplo de código de exemplo VListVW. Ele contém as seções a seguir:

-   [Descrição](#description)
-   [Requisitos mínimos](#minimum-requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

O exemplo de VListVW mostra como implementar um controle de exibição de lista virtual simples em um aplicativo. Um controle de exibição de lista virtual é um controle de exibição de lista padrão com o estilo **LVS \_ OWNERDATA** . Este exemplo cria um controle de exibição de lista que "virtualmente" contém 100.000 itens. Os itens nunca são adicionados de fato. Em vez disso, o controle de exibição de lista virtual é "informado" quantos itens ele contém com a mensagem do [**LVM \_ setitemcount**](lvm-setitemcount.md) . Quando um item precisa ser desenhado, o controle List-View consulta a janela pai para exibir informações com a notificação [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .

## <a name="minimum-requirements"></a>Requisitos mínimos



| Produto          | Versão                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll versão 4,70             |
| Sistema operacional | Windows 95, Microsoft Windows NT 3,51 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

o exemplo de VListVW está disponível no github no [repositório de amostras clássicas do Windows](https://github.com/microsoft/Windows-classic-samples). Os exemplos de itens de controle de exibição de lista podem ser encontrados [aqui](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)

 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo usando o prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto.
2.  Digite `msbuild [project file]`.

Para criar o exemplo usando Visual Studio:

1.  abra Windows Explorer e navegue até o diretório do projeto.
2.  Clique duas vezes no ícone do arquivo. vcproj para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução** para compilar a solução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles de List-View](list-view-controls-overview.md)
</dt> </dl>

 

 




