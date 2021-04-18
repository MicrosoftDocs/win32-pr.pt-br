---
description: As chaves do registro Run e RunOnce fazem com que os programas sejam executados cada vez que um usuário faz logon.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Chaves do registro Run e RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89cf51ad3c7e2096aeffbbd6ed98c02a202f2ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754103"
---
# <a name="run-and-runonce-registry-keys"></a>Chaves do registro Run e RunOnce

As chaves do registro Run e RunOnce fazem com que os programas sejam executados cada vez que um usuário faz logon. O valor de dados de uma chave é uma linha de comando que não tem mais de 260 caracteres. Registre programas para serem executados adicionando entradas da forma linha de -  = *comando* String de descrição. Você pode gravar várias entradas em uma chave. Se mais de um programa estiver registrado em qualquer chave específica, a ordem em que esses programas serão executados será indeterminada.

O registro do Windows inclui as quatro chaves Run e RunOnce a seguir:

-   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Execute**
-   **HKEY \_ atual \_ \\ software \\ do usuário Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ Current \_ user \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

Por padrão, o valor de uma chave RunOnce é excluído antes da execução da linha de comando. Você pode prefixar um nome de valor RunOnce com um ponto de exclamação (!) para adiar a exclusão do valor até que o comando seja executado. Sem o prefixo do ponto de exclamação, se a operação RunOnce falhar, o programa associado não será solicitado a ser executado na próxima vez que você iniciar o computador.

Por padrão, essas chaves são ignoradas quando o computador é iniciado no modo de segurança. O nome do valor das chaves RunOnce pode ser prefixado com um asterisco ( \* ) para forçar o programa a ser executado mesmo no modo de segurança.

Um programa executado de qualquer uma dessas chaves não deve gravar na chave durante sua execução, pois isso irá interferir na execução de outros programas registrados sob a chave. Os aplicativos devem usar a chave RunOnce somente para condições transitórias, como para concluir a instalação do aplicativo. Um aplicativo não deve recriar continuamente entradas em RunOnce porque isso irá interferir com Instalação do Windows.
