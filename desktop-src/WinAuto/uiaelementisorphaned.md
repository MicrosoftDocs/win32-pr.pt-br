---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788732"
---
# <a name="uiaelementisorphaned"></a>UiaElementIsOrphaned

## <a name="text"></a>Texto

O elemento é um AutomationElement órfão na árvore

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O endereço da interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) do objeto obtido para as coordenadas fornecidas é uma referência a um elemento órfão na árvore de elementos.

Esse problema é um problema para as pessoas que contam com um leitor de tela e um teclado para navegação porque os elementos serão tratados como invisíveis e não serão anunciados para o usuário.

## <a name="possible-causes"></a>Possíveis causas

-   A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.
-   Uma implementação de automação de interface do usuário incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAutomationElement.ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




