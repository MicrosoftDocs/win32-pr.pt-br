---
description: Este tópico descreve os tipos de classes de janela, como o sistema as localiza e os elementos que definem o comportamento padrão das janelas que pertencem a elas.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Classes de janela (Windows e mensagens)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b570309ce6613f3adfe256faff9c30b66f9dbd5062de5f342b434be32dce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849501"
---
# <a name="window-classes-windows-and-messages"></a>Classes de janela (Windows e mensagens)

Este tópico descreve os tipos de classes de janela, como o sistema as localiza e os elementos que definem o comportamento padrão das janelas que pertencem a elas.

Uma classe de janela é um conjunto de atributos que o sistema usa como um modelo para criar uma janela. Cada janela é membro de uma classe de janela. Todas as classes de janela são específicas do processo.

### <a name="in-this-section"></a>Nesta seção



| Nome                                                 | Descrição                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre classes de janela](about-window-classes.md)     | Discute classes de janela. Cada classe de janela tem um procedimento de janela associado compartilhado por todas as janelas da mesma classe. O procedimento de janela processa mensagens para todas as janelas dessa classe e, portanto, controla seu comportamento e aparência.<br/> |
| [Usando classes de janela](using-window-classes.md)     | Demonstra como registrar uma janela local e usá-la para criar uma janela principal.<br/>                                                                                                                                                                     |
| [Referência da classe Window](window-class-reference.md) | Contém a referência de API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Funções de classe window



| Nome                                         | Descrição                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Recupera informações sobre uma classe de janela, incluindo um handle para o ícone pequeno associado à classe de janela. A [**função GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) não recupera um alça para o ícone pequeno.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Recupera o valor especificado de 32 bits (**long**) da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associada à janela especificada. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Recupera o valor especificado da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associada à janela especificada.<br/>                                                                                            |
| [**Getclassname**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Recupera o nome da classe à qual a janela especificada pertence. <br/>                                                                                                                                            |
| [**Getwindowlong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Recupera informações sobre a janela especificada. A função também recupera o valor de 32 bits (**long**) no deslocamento especificado para a memória de janela extra.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Recupera informações sobre a janela especificada. A função também recupera o valor em um deslocamento especificado na memória de janela extra.<br/>                                                                        |
| [**Registerclass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registra uma classe de janela para uso subsequente em chamadas para a [**função CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)<br/>                                                             |
| [**Registerclassex**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registra uma classe de janela para uso subsequente em chamadas para a [**função CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Substitui o valor especificado no deslocamento especificado na memória de classe extra ou na estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) da classe à qual a janela especificada pertence.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Substitui o valor de 16 bits (**WORD**) no deslocamento especificado para a memória de classe extra da classe de janela à qual a janela especificada pertence.<br/>                                                               |
| [**Setwindowlong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Altera um atributo da janela especificada. A função também define o valor de 32 bits (longo) no deslocamento especificado para a memória de janela extra.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Altera um atributo da janela especificada. A função também define um valor no deslocamento especificado na memória de janela extra.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Aninha uma classe de janela, liberando a memória necessária para a classe . <br/>                                                                                                                                            |



 

As funções a seguir estão obsoletas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>Getclassinfo</strong></a></td>
<td>Recupera informações sobre uma classe de janela. <br/>
<blockquote>
[!Note]<br />
A <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>função GetClassInfo</strong></a> foi superada pela <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>função GetClassInfoEx.</strong></a> No entanto, você <strong>ainda poderá usar GetClassInfo</strong>se não precisar de informações sobre o ícone pequeno da classe.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></td>
<td>Recupera o valor de 16 bits (<strong>WORD</strong>) no deslocamento especificado para a memória de classe extra da classe de janela à qual a janela especificada pertence.
<blockquote>
[!Note]<br />
Essa função foi preterida para qualquer uso diferente de <em>nIndex definido</em> como GCW_ATOM. A função é fornecida apenas para compatibilidade com versões de 16 bits do Windows. Os aplicativos devem usar <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>a função GetClassLong.</strong></a>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></td>
<td>Substitui o valor de 32 bits (<strong>longo)</strong>especificado no deslocamento especificado para a memória de classe extra ou a estrutura <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> para a classe à qual a janela especificada pertence.
<blockquote>
[!Note]<br />
Essa função foi superada pela <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>função SetClassLongPtr.</strong></a> Para escrever código compatível com versões de 32 e 64 bits do Windows, use <strong>SetClassLongPtr</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a>Estruturas de classe window



| Nome                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contém os atributos de classe de janela registrados pela [**função RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) <br/> Essa estrutura foi superada pela estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) usada com a [**função RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Você ainda poderá usar [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) se não precisar definir o ícone pequeno associado à classe de janela.<br/>                                                  |
| [**Wndclassex**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contém informações de classe de janela. Ele é usado com [**as funções RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) e [**GetClassInfoEx.**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) <br/> A [**estrutura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) é semelhante à [**estrutura WNDCLASS.**](/windows/win32/api/winuser/ns-winuser-wndclassa) Há duas diferenças. **WNDCLASSEX** inclui o membro **cbSize,** que especifica o tamanho da estrutura e o membro **hIconSm,** que contém um handle para um pequeno ícone associado à classe de janela.<br/> |



 

 

 
