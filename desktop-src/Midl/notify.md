---
title: notificar atributo
description: O atributo \ Notify \ instrui o compilador MIDL a gerar uma chamada para um procedimento \ Notify \ no lado do servidor do aplicativo.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notificar MIDL do atributo
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498852"
---
# <a name="notify-attribute"></a><span data-ttu-id="6c3c7-104">notificar atributo</span><span class="sxs-lookup"><span data-stu-id="6c3c7-104">notify attribute</span></span>

<span data-ttu-id="6c3c7-105">O atributo **\[ Notify \]** instrui o compilador MIDL a gerar uma chamada para um procedimento de **\[ notificação \]** no lado do servidor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="6c3c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c3c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3c7-107">*nome do procedimento*</span><span class="sxs-lookup"><span data-stu-id="6c3c7-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6c3c7-108">O nome do procedimento remoto com o qual o procedimento de notificação será associado.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c3c7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c3c7-109">Remarks</span></span>

<span data-ttu-id="6c3c7-110">O procedimento **\[ Notify \]** chamado como resultado do atributo **\[ Notify \]** é associado a um procedimento remoto específico no servidor.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="6c3c7-111">Ele é semelhante em conceito a uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="6c3c7-112">O stub chama o procedimento **\[ Notify \]** depois que todos os argumentos de saída do procedimento remoto ao qual ele está associado tenham sido empacotados e qualquer memória associada aos parâmetros for liberada.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="6c3c7-113">A rotina de **\[ notificação \]** é chamada se uma chamada falhar antes da execução da rotina do servidor.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="6c3c7-114">Por exemplo, se um servidor falhar durante o desempacotamento devido ao recebimento de dados inválidos do cliente, a \[ rotina de notificação \] será chamada.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="6c3c7-115">O atributo **\[ Notify \]** é útil para desenvolver aplicativos que adquirem recursos em procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="6c3c7-116">Esses recursos são liberados no procedimento **\[ Notify \]** depois que os parâmetros de saída do procedimento remoto são totalmente empacotados.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="6c3c7-117">O nome do procedimento de **\[ notificação \]** é o nome do procedimento remoto sufixado por **\_ Notify**.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="6c3c7-118">O procedimento **\_ Notify** não requer nenhum parâmetro e não retorna um resultado.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="6c3c7-119">Um protótipo desse procedimento também é gerado no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6c3c7-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="6c3c7-120">Por exemplo, se o arquivo IDL contiver o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6c3c7-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="6c3c7-121">Especifique o seguinte no ACF para MIDL para gerar a chamada de **\_ notificação** :</span><span class="sxs-lookup"><span data-stu-id="6c3c7-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="6c3c7-122">O compilador MIDL irá gerar o código stub do servidor que contém a seguinte chamada para o procedimento **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="6c3c7-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="6c3c7-123">O arquivo de cabeçalho conterá um protótipo:</span><span class="sxs-lookup"><span data-stu-id="6c3c7-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="6c3c7-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c3c7-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="6c3c7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c3c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3c7-126">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="6c3c7-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 




