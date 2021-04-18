---
description: Solução de problemas
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810539"
---
# <a name="troubleshooting"></a><span data-ttu-id="ee571-103">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="ee571-103">Troubleshooting</span></span>

<span data-ttu-id="ee571-104">Se você estiver tendo problemas para diagnosticar os erros do aplicativo, consulte as seguintes dicas de solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="ee571-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="ee571-105">Verifique se o Coordenador de Transações Distribuídas (DTC) está em execução em todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="ee571-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="ee571-106">Verifique a comunicação de rede testando primeiro em um computador local para verificar se o aplicativo funciona.</span><span class="sxs-lookup"><span data-stu-id="ee571-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="ee571-107">Se você estiver executando o TCP/IP em sua rede, poderá usar o utilitário ping.exe para verificar se os computadores estão na rede.</span><span class="sxs-lookup"><span data-stu-id="ee571-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="ee571-108">Verifique se o SQL e o DTC estão localizados no mesmo computador ou se o programa de configuração do cliente DTC especifica que o DTC está em outro computador.</span><span class="sxs-lookup"><span data-stu-id="ee571-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="ee571-109">Caso contrário, o SQLConnect retornará um erro internamente quando chamado de um componente transacional.</span><span class="sxs-lookup"><span data-stu-id="ee571-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="ee571-110">Defina o tempo limite da transação para um número mais alto que o padrão de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="ee571-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="ee571-111">Depois que o tempo limite da transação tiver decorrido, o COM+ anulará a transação.</span><span class="sxs-lookup"><span data-stu-id="ee571-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="ee571-112">Todas as chamadas subsequentes para o componente retornam imediatamente com o contexto \_ E \_ anulado.</span><span class="sxs-lookup"><span data-stu-id="ee571-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="ee571-113">Certifique-se de que os drivers ODBC sejam thread-safe e não tenham afinidade de thread.</span><span class="sxs-lookup"><span data-stu-id="ee571-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="ee571-114">Se você tiver dificuldade em fazer com que um aplicativo funcione em vários servidores, reinicialize o cliente e verifique se o controlador de domínio está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="ee571-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee571-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee571-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee571-116">Política de FailFast e isolamento de falhas</span><span class="sxs-lookup"><span data-stu-id="ee571-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="ee571-117">Localizando a origem de um erro</span><span class="sxs-lookup"><span data-stu-id="ee571-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="ee571-118">Como o COM+ modifica valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ee571-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="ee571-119">Interpretando códigos de erro</span><span class="sxs-lookup"><span data-stu-id="ee571-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="ee571-120">Estratégias para lidar com erros no COM+</span><span class="sxs-lookup"><span data-stu-id="ee571-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



