---
description: Localizando a origem de um erro
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Localizando a origem de um erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010263"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="86e6e-103">Localizando a origem de um erro</span><span class="sxs-lookup"><span data-stu-id="86e6e-103">Finding the Source of an Error</span></span>

<span data-ttu-id="86e6e-104">Você pode diagnosticar a origem e obter uma descrição dos erros do aplicativo usando COM+ e outras ferramentas.</span><span class="sxs-lookup"><span data-stu-id="86e6e-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="86e6e-105">Se você descobrir que o erro do aplicativo é causado por COM+, poderá interpretar a mensagem de erro exibindo o arquivo Winerror. h ou usando o utilitário de erro Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="86e6e-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="86e6e-106">Se o aplicativo do servidor estiver falhando ou causando um comportamento inesperado, primeiro você deverá determinar onde ocorreu o erro.</span><span class="sxs-lookup"><span data-stu-id="86e6e-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="86e6e-107">O sistema Visualizador de Eventos rastreia eventos de aplicativo, segurança e sistema.</span><span class="sxs-lookup"><span data-stu-id="86e6e-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="86e6e-108">Muitos erros "silenciosos" são registrados aqui.</span><span class="sxs-lookup"><span data-stu-id="86e6e-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="86e6e-109">No entanto, nem todos os erros são mostrados no Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="86e6e-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="86e6e-110">Primeiro, você deve consultar o log do aplicativo no Visualizador de Eventos para verificar o aplicativo associado à mensagem do evento.</span><span class="sxs-lookup"><span data-stu-id="86e6e-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="86e6e-111">(Como você também pode arquivar logs de eventos, é possível acompanhar um histórico de eventos do erro.) Clicar duas vezes em uma entrada no log ativa uma página de **Propriedades do evento** , que fornece mais informações sobre o evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="86e6e-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="86e6e-112">Para obter mais informações sobre como depurar um aplicativo COM+, consulte [Depurando aplicativos com+](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="86e6e-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e6e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86e6e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e6e-114">Política de FailFast e isolamento de falhas</span><span class="sxs-lookup"><span data-stu-id="86e6e-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="86e6e-115">Como o COM+ modifica valores de retorno</span><span class="sxs-lookup"><span data-stu-id="86e6e-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="86e6e-116">Interpretando códigos de erro</span><span class="sxs-lookup"><span data-stu-id="86e6e-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="86e6e-117">Estratégias para lidar com erros no COM+</span><span class="sxs-lookup"><span data-stu-id="86e6e-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="86e6e-118">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="86e6e-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



