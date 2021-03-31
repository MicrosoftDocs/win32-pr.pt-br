---
title: CallFailureLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre as chamadas com falha para os componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- COM valor do registro CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822503"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="b3b5a-104">CallFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="b3b5a-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="b3b5a-105">Define o detalhamento das entradas do log de eventos sobre as chamadas com falha para os componentes.</span><span class="sxs-lookup"><span data-stu-id="b3b5a-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b3b5a-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="b3b5a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="b3b5a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3b5a-107">Remarks</span></span>

<span data-ttu-id="b3b5a-108">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b3b5a-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="b3b5a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b3b5a-109">Value</span></span> | <span data-ttu-id="b3b5a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3b5a-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b5a-111">1</span><span class="sxs-lookup"><span data-stu-id="b3b5a-111">1</span></span>     | <span data-ttu-id="b3b5a-112">Sempre Registre falhas durante uma chamada no processo do servidor COM.</span><span class="sxs-lookup"><span data-stu-id="b3b5a-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="b3b5a-113">2</span><span class="sxs-lookup"><span data-stu-id="b3b5a-113">2</span></span>     | <span data-ttu-id="b3b5a-114">Nunca Registre falhas durante uma chamada no processo do servidor COM.</span><span class="sxs-lookup"><span data-stu-id="b3b5a-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="b3b5a-115">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="b3b5a-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b3b5a-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3b5a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3b5a-117">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="b3b5a-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




