---
description: Como a API de instalação não fornece uma rotina de retorno de chamada de gabinete padrão, você precisa fornecer uma rotina. A rotina de retorno de chamada que a função SetupIterateCabinet requer deve ter a mesma forma que aquelas apontadas por filecallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Criando uma rotina de retorno de chamada de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169824"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="011ce-104">Criando uma rotina de retorno de chamada de gabinete</span><span class="sxs-lookup"><span data-stu-id="011ce-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="011ce-105">Como a API de instalação não fornece uma rotina de retorno de chamada de gabinete padrão, você precisa fornecer uma rotina.</span><span class="sxs-lookup"><span data-stu-id="011ce-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="011ce-106">A rotina de retorno de chamada que a função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) requer deve ter a mesma forma que aquelas apontadas por [filecallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="011ce-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="011ce-107">Veja a seguir a sintaxe que o [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) usa para enviar uma notificação para a rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="011ce-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="011ce-108">O parâmetro de *contexto* é um ponteiro void para uma variável de contexto ou estrutura que pode ser usada pela rotina de retorno de chamada para armazenar informações que precisam persistir entre chamadas subsequentes para a rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="011ce-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="011ce-109">A implementação desse contexto é especificada pela rotina de retorno de chamada e nunca é referenciada ou alterada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="011ce-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="011ce-110">O parâmetro de *notificação* é um inteiro não assinado e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="011ce-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="011ce-111">Notificação</span><span class="sxs-lookup"><span data-stu-id="011ce-111">Notification</span></span>                                                        | <span data-ttu-id="011ce-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="011ce-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="011ce-113">**SPFILENOTIFY \_ extraied**</span><span class="sxs-lookup"><span data-stu-id="011ce-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="011ce-114">O arquivo foi extraído do gabinete.</span><span class="sxs-lookup"><span data-stu-id="011ce-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="011ce-115">**SPFILENOTIFY \_ FILEINCABINET**</span><span class="sxs-lookup"><span data-stu-id="011ce-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="011ce-116">Um arquivo é encontrado no gabinete.</span><span class="sxs-lookup"><span data-stu-id="011ce-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="011ce-117">**SPFILENOTIFY \_ NEEDNEWCABINET**</span><span class="sxs-lookup"><span data-stu-id="011ce-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="011ce-118">O arquivo atual continua no próximo gabinete.</span><span class="sxs-lookup"><span data-stu-id="011ce-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="011ce-119">Os dois últimos parâmetros, *param1* e *param2*, também são inteiros sem sinal e contêm informações adicionais relevantes para a notificação.</span><span class="sxs-lookup"><span data-stu-id="011ce-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="011ce-120">Para obter mais informações sobre as notificações enviadas pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), consulte [notificação de arquivo de gabinete](cabinet-file-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="011ce-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="011ce-121">Uma \_ rotina de \_ retorno de chamada notificar arquivo do SP \_ retorna um inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="011ce-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="011ce-122">A rotina de retorno de chamada do gabinete deve retornar um dos valores a seguir, dependendo da notificação.</span><span class="sxs-lookup"><span data-stu-id="011ce-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="011ce-123">Para a \_ notificação SPFILENOTIFY FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) espera que um dos valores a seguir seja retornado pela rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="011ce-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="011ce-124">Valor</span><span class="sxs-lookup"><span data-stu-id="011ce-124">Value</span></span>         | <span data-ttu-id="011ce-125">Significado</span><span class="sxs-lookup"><span data-stu-id="011ce-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="011ce-126">\_anular FILEOP</span><span class="sxs-lookup"><span data-stu-id="011ce-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="011ce-127">Anular o processamento do gabinete.</span><span class="sxs-lookup"><span data-stu-id="011ce-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="011ce-128">FILEOP \_ doit</span><span class="sxs-lookup"><span data-stu-id="011ce-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="011ce-129">Extraia o arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="011ce-129">Extract the current file.</span></span> |
| <span data-ttu-id="011ce-130">FILEOP \_ ignorar</span><span class="sxs-lookup"><span data-stu-id="011ce-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="011ce-131">Ignorar o arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="011ce-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="011ce-132">Para \_ notificações SPFILENOTIFY NEEDNEWCABINET e SPFILENOTIFY extracçãod \_ , **SetupIterateCabinet** espera que um dos valores a seguir seja retornado pela rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="011ce-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="011ce-133">Valor</span><span class="sxs-lookup"><span data-stu-id="011ce-133">Value</span></span>      | <span data-ttu-id="011ce-134">Significado</span><span class="sxs-lookup"><span data-stu-id="011ce-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="011ce-135">SEM \_ erros</span><span class="sxs-lookup"><span data-stu-id="011ce-135">NO\_ERROR</span></span>  | <span data-ttu-id="011ce-136">Nenhum erro foi encontrado, continue processando o gabinete.</span><span class="sxs-lookup"><span data-stu-id="011ce-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="011ce-137">ERRO \_ xxx</span><span class="sxs-lookup"><span data-stu-id="011ce-137">ERROR\_XXX</span></span> | <span data-ttu-id="011ce-138">Ocorreu um erro do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="011ce-138">An error of the specified type occurred.</span></span> <span data-ttu-id="011ce-139">A função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará **false** e o código de erro especificado será retornado por uma chamada para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="011ce-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="011ce-140">Se a rotina de retorno de chamada retornar FILEOP \_ doit, a rotina também deverá fornecer um caminho de destino completo.</span><span class="sxs-lookup"><span data-stu-id="011ce-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="011ce-141">Para obter mais informações, consulte [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).</span><span class="sxs-lookup"><span data-stu-id="011ce-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
