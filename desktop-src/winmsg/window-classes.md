---
description: Este tópico descreve os tipos de classes de janela, como o sistema as localiza e os elementos que definem o comportamento padrão do Windows que pertencem a elas.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Classes de janela (Windows e mensagens)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77e96a06433bf6bbcb72fb76a41a29fccee27ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482642"
---
# <a name="window-classes-windows-and-messages"></a>Classes de janela (Windows e mensagens)

Este tópico descreve os tipos de classes de janela, como o sistema as localiza e os elementos que definem o comportamento padrão do Windows que pertencem a elas.

Uma classe de janela é um conjunto de atributos que o sistema usa como um modelo para criar uma janela. Cada janela é membro de uma classe de janela. Todas as classes de janela são específicas de processo.

### <a name="in-this-section"></a>Nesta seção



| Nome                                                 | Descrição                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre classes de janela](about-window-classes.md)     | Discute as classes de janela. Cada classe de janela tem um procedimento de janela associado compartilhado por todas as janelas da mesma classe. O procedimento de janela processa mensagens para todas as janelas dessa classe e, portanto, controla seu comportamento e aparência.<br/> |
| [Usando classes de janela](using-window-classes.md)     | Demonstra como registrar uma janela local e usá-la para criar uma janela principal.<br/>                                                                                                                                                                     |
| [Referência de classe de janela](window-class-reference.md) | Contém a referência de API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Funções de classe de janela



| Nome                                         | Descrição                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Recupera informações sobre uma classe de janela, incluindo um identificador para o ícone pequeno associado à classe de janela. A função [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) não recupera um identificador para o ícone pequeno.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Recupera o valor especificado de 32 bits (**longo**) da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associada à janela especificada. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Recupera o valor especificado da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associada à janela especificada.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Recupera o nome da classe à qual a janela especificada pertence. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Recupera informações sobre a janela especificada. A função também recupera o valor de 32 bits (**longo**) no deslocamento especificado na memória da janela extra.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Recupera informações sobre a janela especificada. A função também recupera o valor em um deslocamento especificado na memória da janela extra.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registra uma classe de janela para uso posterior em chamadas para a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registra uma classe de janela para uso posterior em chamadas para a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Substitui o valor especificado no deslocamento especificado na memória da classe extra ou na estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) da classe à qual a janela especificada pertence.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Substitui o valor de 16 bits (**Word**) no deslocamento especificado na memória de classe extra da classe Window à qual a janela especificada pertence.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Altera um atributo da janela especificada. A função também define o valor de 32 bits (longo) no deslocamento especificado na memória da janela extra.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Altera um atributo da janela especificada. A função também define um valor no deslocamento especificado na memória da janela extra.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Cancela o registro de uma classe de janela, liberando a memória necessária para a classe. <br/>                                                                                                                                            |



 

As funções a seguir são obsoletas.




| Nome | Descrição | 
|------|-------------|
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> | Recupera informações sobre uma classe de janela. <br /><blockquote>[!Note]<br />A função <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> foi substituída pela função <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a> . No entanto, você ainda poderá usar <strong>GetClassInfo</strong>se não precisar de informações sobre o ícone de classe pequena.</blockquote><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a> | Recupera o valor de 16 bits (<strong>Word</strong>) no deslocamento especificado na memória de classe extra para a classe de janela à qual a janela especificada pertence.<blockquote>[!Note]<br />Essa função foi preterida para qualquer uso diferente de <em>nIndex</em> definido como GCW_ATOM. A função é fornecida somente para compatibilidade com versões de 16 bits do Windows. Os aplicativos devem usar a função <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> .</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a> | Substitui o valor especificado de 32 bits (<strong>longo</strong>) no deslocamento especificado na memória da classe extra ou na estrutura <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> da classe à qual a janela especificada pertence.<blockquote>[!Note]<br />Essa função foi substituída pela função <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> . para escrever código compatível com as versões de 32 bits e 64 bits do Windows, use <strong>SetClassLongPtr</strong>.</blockquote><br /><br /> | 




 

### <a name="window-class-structures"></a>Estruturas de classe de janela



| Nome                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contém os atributos de classe de janela que são registrados pela função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . <br/> Essa estrutura foi substituída pela estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) usada com a função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Você ainda poderá usar [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) se não precisar definir o ícone pequeno associado à classe de janela.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contém informações de classe de janela. Ele é usado com as funções [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) e [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  . <br/> A estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) é semelhante à estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Há duas diferenças. **WNDCLASSEX** inclui o membro **cbSize** , que especifica o tamanho da estrutura e o membro **hIconSm** , que contém um identificador para um pequeno ícone associado à classe Window.<br/> |



 

 

 
