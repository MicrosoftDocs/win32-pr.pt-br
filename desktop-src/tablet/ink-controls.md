---
description: Visão geral dos controles de tinta para o Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controles de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501627"
---
# <a name="ink-controls"></a>Controles de tinta

A plataforma do Tablet PC fornece dois controles, [InkEdit](inkedit-control.md) e [InkPicture](inkpicture-control.md), que permitem adicionar facilmente a tinta e o reconhecimento de manuscrito aos aplicativos do Tablet PC. O controle InkEdit tem versões [gerenciadas](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) e Win32, enquanto a InkPicture tem apenas as versões gerenciadas e [ActiveX](inkpicture-control-reference.md) do [InkPicture](/previous-versions/ms583740(v=vs.100)) .

A principal diferença entre os controles é a forma como os dados são salvos. O controle [InkEdit](inkedit-control.md) salva a tinta como texto por padrão, enquanto a [InkPicture](inkpicture-control.md) salva a tinta como tinta.

O controle [InkEdit](inkedit-control.md) destina-se à entrada de texto por meio do reconhecimento de manuscrito. O [InkPicture](inkpicture-control.md) destina-se à anotação (por exemplo, marcando um slide de apresentação ou outra imagem).

Em código gerenciado, crie controles de tinta no mesmo thread que o thread principal para o formulário. Se um controle [InkEdit](inkedit-control.md) ou [InkPicture](inkpicture-control.md) for criado em um thread diferente, o aplicativo poderá não responder corretamente.

Você deve alterar explicitamente o modelo de threading para single-thread apartment (STA) antes de criar um controle de tinta. Isso faz com que o controle seja criado no thread principal. Você pode usar o seguinte código C++ gerenciado para definir explicitamente o modelo de Threading.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Você pode usar o código a seguir para fazer a mesma coisa em C \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Em código gerenciado, para evitar um vazamento de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer controle do Tablet PC ao qual um manipulador de eventos tenha sido anexado antes que o controle saia do escopo.

As seções a seguir descrevem os controles de tinta e o uso de controles de tinta em aplicativos:

-   [Adicionando controles de tinta a um projeto](adding-ink-controls-to-a-project.md)
-   [Controle InkEdit](inkedit-control.md)
-   [Controle InkPicture](inkpicture-control.md)

 

 
