---
description: Executar e executar chaves do Registro do RunOnce faz com que os programas executem sempre que um usuário faz login.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Executar e executar chaves do Registro do RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e69559a1034e3dcdb6eae215400d475fb9ca8be4025a38d064e914837af8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665236"
---
# <a name="run-and-runonce-registry-keys"></a>Executar e executar chaves do Registro do RunOnce

Executar e executar chaves do Registro do RunOnce faz com que os programas executem sempre que um usuário faz login. O valor de dados de uma chave é uma linha de comando que não tem mais de 260 caracteres. Registre programas para executar adicionando entradas da linha de comando da cadeia de caracteres de *descrição* -  = *do formulário*. Você pode gravar várias entradas em uma chave. Se mais de um programa estiver registrado em qualquer chave específica, a ordem na qual esses programas são executados será indeterminada.

O Windows registro inclui as quatro chaves Run e RunOnce a seguir:

-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**

Por padrão, o valor de uma chave RunOnce é excluído antes da linha de comando ser executado. Você pode prefixar um nome de valor RunOnce com um ponto de exclamação (!) para adiar a exclusão do valor até que o comando seja executado. Sem o prefixo do ponto de exclamação, se a operação RunOnce falhar, o programa associado não será solicitado a executar na próxima vez que você iniciar o computador.

Por padrão, essas chaves são ignoradas quando o computador é iniciado no Cofre Modo. O nome do valor das chaves RunOnce pode ser prefixado com um asterisco ( ) para forçar o programa a ser executado mesmo \* no modo Cofre.

Um programa executado de qualquer uma dessas chaves não deve gravar na chave durante sua execução, pois isso interferirá na execução de outros programas registrados na chave. Os aplicativos devem usar a chave RunOnce somente para condições transitórias, como para concluir a configuração do aplicativo. Um aplicativo não deve recriar continuamente entradas em RunOnce porque isso interferirá na Windows Configuração.
