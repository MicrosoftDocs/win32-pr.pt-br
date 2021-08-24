---
description: O modo de erro indica ao sistema como o aplicativo vai responder a erros graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modo de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1baa4c0bc4e1209586b630f2a58bfb06572131de8e7d2706614c78646d7e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260925"
---
# <a name="error-mode"></a>Modo de erro

O modo de erro indica ao sistema como o aplicativo vai responder a erros graves. Erros graves incluem falha de disco, erros de unidade não pronta, desalinhamento de dados e exceções sem tratamento. Esse modo de erro pode ser gerenciado por thread ou por processo. Um aplicativo pode deixar o sistema exibir uma caixa de mensagem informando ao usuário que ocorreu um erro ou pode manipular os erros.

Para lidar com esses erros sem a intervenção do usuário, use [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ou o [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)específico do thread. Depois de chamar uma dessas funções e especificar os sinalizadores apropriados, o sistema não exibirá as caixas de mensagem de erro correspondentes.

Um processo pode recuperar seu modo de erro usando [**Geterromode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) ou [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).

A prática recomendada é que todos os aplicativos chamem a função [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) de todo o processo com um parâmetro de **sem \_ FAILCRITICALERRORS** na inicialização. Isso é para evitar que as caixas de diálogo do modo de erro deslocassem o aplicativo.

Além disso, os chamadores devem favorecer as versões específicas de thread dessas funções, pois elas são menos interrupções no comportamento normal do sistema.

 

 
