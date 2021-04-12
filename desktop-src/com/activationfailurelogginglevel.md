---
title: ActivationFailureLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre solicitações com falha para inicialização e ativação do componente.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- COM valor do registro ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364443"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="5a783-104">ActivationFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="5a783-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="5a783-105">Define o detalhamento das entradas do log de eventos sobre solicitações com falha para inicialização e ativação do componente.</span><span class="sxs-lookup"><span data-stu-id="5a783-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5a783-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="5a783-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="5a783-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a783-107">Remarks</span></span>

<span data-ttu-id="5a783-108">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5a783-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="5a783-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5a783-109">Value</span></span> | <span data-ttu-id="5a783-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a783-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a783-111">0</span><span class="sxs-lookup"><span data-stu-id="5a783-111">0</span></span>     | <span data-ttu-id="5a783-112">Use o registro em log discricionário.</span><span class="sxs-lookup"><span data-stu-id="5a783-112">Use discretionary logging.</span></span> <span data-ttu-id="5a783-113">Falhas de log por padrão, mas os clientes podem substituir esse comportamento especificando \_ CLSCTX \_ nenhum \_ log de falha em [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span><span class="sxs-lookup"><span data-stu-id="5a783-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="5a783-114">Este é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="5a783-114">This is the default value.</span></span> |
| <span data-ttu-id="5a783-115">1</span><span class="sxs-lookup"><span data-stu-id="5a783-115">1</span></span>     | <span data-ttu-id="5a783-116">Sempre Registre todas as falhas, independentemente do que o cliente especificou.</span><span class="sxs-lookup"><span data-stu-id="5a783-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="5a783-117">2</span><span class="sxs-lookup"><span data-stu-id="5a783-117">2</span></span>     | <span data-ttu-id="5a783-118">Nunca registre nenhuma falha, independentemente do que o cliente especificou.</span><span class="sxs-lookup"><span data-stu-id="5a783-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="5a783-119">Se você precisar de um aplicativo para controlar o log de eventos, é recomendável que você defina esse valor como 0 e grave o código do cliente para substituí-lo quando necessário.</span><span class="sxs-lookup"><span data-stu-id="5a783-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="5a783-120">É altamente recomendável que você não defina o valor como 2.</span><span class="sxs-lookup"><span data-stu-id="5a783-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="5a783-121">Se o log de eventos estiver desabilitado, será mais difícil diagnosticar problemas.</span><span class="sxs-lookup"><span data-stu-id="5a783-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="5a783-122">Para falhas de permissão de restrições de máquina, em que COM não tem os bits CLSCTX, o COM tratará um valor de 0 como 1.</span><span class="sxs-lookup"><span data-stu-id="5a783-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a783-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a783-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a783-124">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="5a783-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




