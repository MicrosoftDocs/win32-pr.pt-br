---
description: Fornece links para códigos de erro do sistema definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Códigos de erro do sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 072e1eb4a43c787055bc2793b3f58d69cdf6dd12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089214"
---
# <a name="system-error-codes"></a>Códigos de erro do sistema

Esta seção destina-se a desenvolvedores que estão Depurando erros de sistema. Se você chegou a esta página durante a pesquisa de outros erros, aqui estão alguns links que podem ajudar:

* [Windows Update erros](https://support.microsoft.com/help/10164/fix-windows-update-errors) -para ajudar a resolver problemas com Windows Update.
* [Erros de ativação do Windows](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) -para obter ajuda para verificar sua cópia do Windows.
* [Solucionando problemas de erros de tela azul](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) -para obter ajuda para descobrir o que causou um erro de parada.
* [Suporte da Microsoft](https://support.microsoft.com) -para obter suporte com um produto da Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Mais maneiras de encontrar um código de erro

Listamos os códigos de erro do sistema nesta seção, organizados por número. Se você precisar de mais ajuda para rastrear um erro específico, aqui estão algumas recomendações:

* Use a [ferramenta de pesquisa de erros da Microsoft](system-error-code-lookup-tool.md).
*  Instale as ferramentas de depuração para Windows, carregue um arquivo de despejo de memória e execute o comando **\! Err \<code>** .
* Pesquise o código de erro ou texto bruto no site de protocolos da Microsoft. Para obter mais informações, consulte [[MS-ERREF]: códigos de erro do Windows](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Códigos de erro de terceiros

Outros códigos de erro podem ser gerados por serviços ou aplicativos de terceiros (por exemplo, o **código de erro:-118** pode ser exibido pelo [serviço de jogo de fluxo](https://support.steampowered.com/kb_cat.php?id=59)) e, nessas situações, você entraria em contato com a linha de suporte de terceiros.

## <a name="system-error-codes"></a>Códigos de erro do sistema

Os códigos de erro do sistema são muito amplos: cada um pode ocorrer em uma das muitas centenas de locais no sistema. Consequentemente, as descrições desses códigos não podem ser muito específicas. O uso desses códigos requer alguma quantidade de investigação e análise. Você precisa observar o contexto de programação e de tempo de execução no qual esses erros ocorrem. 

Como esses códigos são definidos no WinError. h para qualquer pessoa usar, às vezes os códigos são retornados por software que não é do sistema. E, às vezes, o código é retornado por uma função profunda na pilha e removido do código que está manipulando o erro.

Os tópicos a seguir fornecem listas de códigos de erro do sistema. Esses valores são definidos no arquivo de cabeçalho WinError. h.

-   [Códigos de erro do sistema (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Códigos de erro do sistema (500-999) (0x1F4-0x3e7)](system-error-codes--500-999-.md)
-   [Códigos de erro do sistema (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Códigos de erro do sistema (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Códigos de erro do sistema (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Códigos de erro do sistema (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Códigos de erro do sistema (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Códigos de erro do sistema (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Códigos de erro do sistema (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Códigos de erro do sistema (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
