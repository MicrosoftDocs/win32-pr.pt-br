---
description: Fornece links para códigos de erro do sistema definidos no arquivo de título WinError.h e destina-se a desenvolvedores.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Códigos de erro do sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 4c762b2098531ecb19ad84522f8c9c8272c004397bbc4b32f15a6f6e157c4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691726"
---
# <a name="system-error-codes"></a>Códigos de erro do sistema

Esta seção destina-se a desenvolvedores que estão depurando erros do sistema. Se você chegou a esta página ao procurar outros erros, aqui estão alguns links que podem ajudar:

* [Windows erros de atualização –](https://support.microsoft.com/help/10164/fix-windows-update-errors) para ajudar a resolver problemas com Windows Atualização.
* [Windows erros de ativação](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) – para ajudar a verificar sua cópia do Windows.
* [Solução de problemas de erros de tela azul](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) – para ajudar a descobrir o que causou um erro de parada.
* [Suporte da Microsoft](https://support.microsoft.com) - para suporte com um produto da Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Mais maneiras de encontrar um código de erro

Listamos os códigos de erro do sistema nesta seção, organizados por número. Se você precisar de mais ajuda para rastrear um erro específico, veja mais algumas recomendações:

* Use a [Ferramenta de Pesquisa de Erros da Microsoft](system-error-code-lookup-tool.md).
*  Instale as Ferramentas de Depuração para Windows, carregue um arquivo de despejo de memória e execute o **\! comando err. \<code>**
* Pesquise o texto bruto ou o código de erro no site do Microsoft Protocols. Para obter mais informações, [consulte [MS-ERREF]: Windows códigos de erro](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Códigos de erro de terceiros

Outros códigos de erro podem ser gerados por serviços ou aplicativos de terceiros (por exemplo, Código de **Erro: -118** pode ser exibido pelo serviço de jogos [do Steam)](https://support.steampowered.com/kb_cat.php?id=59)e, nessas situações, você entraria em contato com a linha de suporte do terceiro.

## <a name="system-error-codes"></a>Códigos de erro do sistema

Os Códigos de Erro do Sistema são muito amplos: cada um deles pode ocorrer em uma das muitas centenas de locais no sistema. Consequentemente, as descrições desses códigos não podem ser muito específicas. O uso desses códigos requer alguma quantidade de investigação e análise. Você precisa observar o contexto programático e de runtime no qual esses erros ocorrem. 

Como esses códigos são definidos em WinError.h para qualquer pessoa usar, às vezes, os códigos são retornados por softwares que não são do sistema. E, às vezes, o código é retornado por uma função no fundo da pilha e distante do código que está tratando o erro.

Os tópicos a seguir fornecem listas de códigos de erro do sistema. Esses valores são definidos no arquivo de título WinError.h.

-   [Códigos de erro do sistema (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Códigos de erro do sistema (500-999) (0x1f4-0x3e7)](system-error-codes--500-999-.md)
-   [Códigos de erro do sistema (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Códigos de erro do sistema (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Códigos de erro do sistema (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Códigos de erro do sistema (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Códigos de erro do sistema (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Códigos de erro do sistema (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Códigos de erro do sistema (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Códigos de erro do sistema (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
