---
description: Quando ocorre um erro, a maioria das funções do sistema retorna um código de erro, geralmente 0, nulo ou &\# 8211; 1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Código de Last-Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bf0fe2f544fc3d87690be81b0d09767745ef95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920202"
---
# <a name="last-error-code"></a>Código de Last-Error

Quando ocorre um erro, a maioria das funções do sistema retorna um código de erro, geralmente 0, **nulo** ou – 1. Muitas funções do sistema também definem um código de erro adicional chamado *código de último erro*. Esse código de erro é mantido separadamente para cada thread em execução; um erro em um thread não substitui o último código de erro em outro thread. Qualquer função pode chamar a função [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) ou [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) para definir o último código de erro para o thread atual. Essas funções são destinadas principalmente às bibliotecas de vínculo dinâmico (DLL), para que possam fornecer informações ao aplicativo de chamada. Observe que algumas funções chamam **SetLastError** ou **SetLastErrorEx** com 0 quando tiverem êxito, apagando o código de erro definido pela função com falha mais recentemente, enquanto outros não.

Um aplicativo pode recuperar o código do último erro usando a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ; o código de erro pode informar mais sobre o que realmente ocorreu para fazer a função falhar. A documentação para funções do sistema indicará as condições sob as quais a função define o último código de erro.

O sistema define um conjunto de códigos de erro que podem ser definidos como códigos de último erro ou retornados por essas funções. Os códigos de erro são valores de 32 bits (o bit 31 é o bit mais significativo). O bit 29 é reservado para códigos de erro definidos pelo aplicativo; nenhum código de erro do sistema tem este conjunto de bits. Se você definir códigos de erro para seu aplicativo, defina esse bit para indicar que o código de erro foi definido por um aplicativo e para garantir que os códigos de erro não entrem em conflito com nenhum código de erro definido pelo sistema. Para obter mais informações, consulte WinError. h e [códigos de erro do sistema](system-error-codes.md).

 

 
