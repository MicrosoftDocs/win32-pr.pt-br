---
description: O modo de erro indica ao sistema como o aplicativo vai responder a erros graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modo de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088843"
---
# <a name="error-mode"></a>Modo de erro

O modo de erro indica ao sistema como o aplicativo vai responder a erros graves. Erros graves incluem falha de disco, erros de unidade não pronta, desalinhamento de dados e exceções sem tratamento. Esse modo de erro pode ser gerenciado por thread ou por processo. Um aplicativo pode deixar o sistema exibir uma caixa de mensagem informando ao usuário que ocorreu um erro ou pode manipular os erros.

Para lidar com esses erros sem a intervenção do usuário, use [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ou o [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)específico do thread. Depois de chamar uma dessas funções e especificar os sinalizadores apropriados, o sistema não exibirá as caixas de mensagem de erro correspondentes.

Um processo pode recuperar seu modo de erro usando [**Geterromode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) ou [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).

A prática recomendada é que todos os aplicativos chamem a função [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) de todo o processo com um parâmetro de **sem \_ FAILCRITICALERRORS** na inicialização. Isso é para evitar que as caixas de diálogo do modo de erro deslocassem o aplicativo.

Além disso, os chamadores devem favorecer as versões específicas de thread dessas funções, pois elas são menos interrupções no comportamento normal do sistema.

 

 
