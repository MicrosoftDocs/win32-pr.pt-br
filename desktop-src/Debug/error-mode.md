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
# <a name="error-mode"></a><span data-ttu-id="fbe53-103">Modo de erro</span><span class="sxs-lookup"><span data-stu-id="fbe53-103">Error Mode</span></span>

<span data-ttu-id="fbe53-104">O modo de erro indica ao sistema como o aplicativo vai responder a erros graves.</span><span class="sxs-lookup"><span data-stu-id="fbe53-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="fbe53-105">Erros graves incluem falha de disco, erros de unidade não pronta, desalinhamento de dados e exceções sem tratamento.</span><span class="sxs-lookup"><span data-stu-id="fbe53-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="fbe53-106">Esse modo de erro pode ser gerenciado por thread ou por processo.</span><span class="sxs-lookup"><span data-stu-id="fbe53-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="fbe53-107">Um aplicativo pode deixar o sistema exibir uma caixa de mensagem informando ao usuário que ocorreu um erro ou pode manipular os erros.</span><span class="sxs-lookup"><span data-stu-id="fbe53-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="fbe53-108">Para lidar com esses erros sem a intervenção do usuário, use [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ou o [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)específico do thread.</span><span class="sxs-lookup"><span data-stu-id="fbe53-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="fbe53-109">Depois de chamar uma dessas funções e especificar os sinalizadores apropriados, o sistema não exibirá as caixas de mensagem de erro correspondentes.</span><span class="sxs-lookup"><span data-stu-id="fbe53-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="fbe53-110">Um processo pode recuperar seu modo de erro usando [**Geterromode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) ou [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span><span class="sxs-lookup"><span data-stu-id="fbe53-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="fbe53-111">A prática recomendada é que todos os aplicativos chamem a função [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) de todo o processo com um parâmetro de **sem \_ FAILCRITICALERRORS** na inicialização.</span><span class="sxs-lookup"><span data-stu-id="fbe53-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="fbe53-112">Isso é para evitar que as caixas de diálogo do modo de erro deslocassem o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fbe53-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="fbe53-113">Além disso, os chamadores devem favorecer as versões específicas de thread dessas funções, pois elas são menos interrupções no comportamento normal do sistema.</span><span class="sxs-lookup"><span data-stu-id="fbe53-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 
