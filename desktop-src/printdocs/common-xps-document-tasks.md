---
description: Esta página lista algumas das tarefas de programação que normalmente são executadas com a API de documento XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tarefas comuns de programação de documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775577"
---
# <a name="common-xps-document-programming-tasks"></a>Tarefas comuns de programação de documentos XPS

Esta página lista algumas das tarefas de programação que normalmente são executadas com a API de documento XPS.

## <a name="common-xps-document-tasks"></a>Tarefas comuns do documento XPS

Os exemplos de código a seguir ilustram algumas das tarefas de programação que normalmente são executadas quando a API de documento XPS é usada para trabalhar com um OM XPS.

<dl>

[Inicializar um OM XPS](xps-object-model-initialization.md)  
[Criar um OM XPS em branco](create-a-blank-xps-om.md)  
[Ler um documento XPS em um OM XPS](read-an-xps-document-into-an-xps-om.md)  
[Navegar no OM XPS](navigate-the-xps-om.md)  
[Gravar texto em um OM XPS](write-text-to-an-xps-om.md)  
[Desenhar gráficos em um OM XPS](draw-graphics-in-an-xps-om.md)  
[Coloque as imagens em um OM XPS](place-images-in-an-xps-om.md)  
[Gravar um OM XPS em um documento XPS](write-an-xps-om-to-an-xps-document.md)  
[Imprimir um OM XPS](print-an-xps-om.md)  
[Trabalhando com interfaces de coleção de OM XPS](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Isenção de responsabilidade

Os exemplos de código não se destinam a serem programas completos e em funcionamento. Os exemplos de código que são referenciados nesta página, por exemplo, não executam verificação de parâmetros, verificação de erros ou tratamento de erros. Use esses exemplos como ponto de partida e, em seguida, adicione o código necessário para criar um aplicativo robusto. Para obter mais informações sobre valores de retorno **HRESULT** e estratégias de tratamento de erros, consulte [tratamento de erros em com](../com/error-handling-in-com.md).

Antes que as interfaces do XPS OM possam ser usadas, o COM deve ser inicializado no thread, conforme mostrado no código de exemplo a seguir.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Para maior clareza, esses exemplos de código usam um OM XPS muito simples, um que pode não ser complexo o suficiente para seu aplicativo. Como um caso no ponto, nos exemplos de código que adicionam conteúdo a uma página, os elementos visuais de uma página são adicionados diretamente à lista de objetos visuais da página; no entanto, na prática, você pode querer agrupar objetos visuais em objetos Canvas, para que vários objetos possam ser afetados como um grupo. Portanto, para habilitar o suporte do mesmo conteúdo para mais de um tamanho de página, você pode agrupar o conteúdo visual de uma página em um único objeto Canvas e, em seguida, aplicar uma transformação à tela para dimensioná-la para o tamanho da página atual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](../com/error-handling-in-com.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
