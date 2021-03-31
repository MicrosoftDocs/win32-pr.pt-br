---
title: API de ampliação
description: A API de ampliação permite que os aplicativos ampliem a tela inteira ou partes da tela e apliquem efeitos de cor.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/08/2020
ms.locfileid: "103823548"
---
# <a name="magnification-api"></a>API de ampliação

## <a name="purpose"></a>Finalidade

A API de ampliação permite que os aplicativos ampliem a tela inteira ou partes da tela e apliquem efeitos de cor.

## <a name="where-applicable"></a>Quando aplicável

Usando a API de ampliação, os desenvolvedores podem criar aplicativos de tecnologia assistencial baseados no Windows que ampliam a tela e aplicam efeitos de cor ao conteúdo da tela ampliado. Para os usuários com deficiência visual, o tamanho de imagem ampliado e os efeitos de cor podem ajudar a facilitar a visualização e o uso do computador.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de ampliação foi projetada principalmente para desenvolvedores de C e C++ que entendem a programação do Windows e que estão familiarizados com os conceitos de programação de elementos gráficos.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A versão inicial da API de ampliação tem suporte no Windows Vista e em sistemas operacionais posteriores. Uma segunda versão adiciona recursos de ampliação de tela inteira e tem suporte no Windows 8 e posterior.

A API é suportada pelo Magnification.dll. Para compilar seu aplicativo, inclua ampliação. h e vincule a ampliação. lib.

> [!Note]  
> A API de ampliação não tem suporte no WOW64; ou seja, um aplicativo de lupa de 32 bits não será executado corretamente em janelas de 64 bits.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|:---|:---|
| [Visão geral da API de ampliação](magapi-intro.md)<br/> | Este tópico descreve a API de ampliação e explica como usá-la em um aplicativo.<br/> |
| [Referência](entry-magapi-ref.md)<br/>  | Esta seção contém informações de referência para a API de ampliação.<br/>|
| [Amostras](magapi-samples-entry.md)<br/> | O exemplo de aplicativo a seguir demonstra como usar a API de ampliação para criar uma lupa de tela inteira que amplia toda a tela e uma lupa em janelas que aumenta e exibe uma parte da tela em uma janela.<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Site de acessibilidade da Microsoft](https://www.microsoft.com/accessibility/), [acessibilidade no Windows 10](/windows/apps/accessibility)
