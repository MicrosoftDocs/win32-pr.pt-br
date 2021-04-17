---
description: Configurando o log de erros
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Configurando o log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754209"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="d315b-103">Configurando o log de erros</span><span class="sxs-lookup"><span data-stu-id="d315b-103">Setting the Error Log</span></span>

<span data-ttu-id="d315b-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="d315b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d315b-105">Depois de implementar a classe de log de erros, crie uma nova instância da classe.</span><span class="sxs-lookup"><span data-stu-id="d315b-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="d315b-106">Em seguida, dê aos [serviços de edição do DirectShow](directshow-editing-services.md) um ponteiro para ele chamando o método [**IAMSetErrorLog::p UT log de \_ erros**](iamseterrorlog-put-errorlog.md) na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="d315b-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="d315b-107">Consulte a linha do tempo para a interface **IAMSetErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="d315b-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="d315b-108">Para garantir que todos os erros sejam registrados, você deve chamar esse método antes de carregar, salvar ou renderizar a linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="d315b-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="d315b-109">O log de erros não tem nenhum efeito sobre os valores de retorno que você recebe ao chamar métodos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d315b-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="d315b-110">O log de erros complementa, mas não substitui as técnicas de tratamento de erros usuais.</span><span class="sxs-lookup"><span data-stu-id="d315b-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="d315b-111">Para criar um aplicativo robusto, sempre verifique os valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d315b-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d315b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d315b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d315b-113">Erros de log</span><span class="sxs-lookup"><span data-stu-id="d315b-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



