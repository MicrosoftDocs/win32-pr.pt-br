---
title: notify_flag atributo
description: O atributo \ notificar \_ sinalizador \ fornece uma notificação identificando se uma rotina de servidor é chamada.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag do atributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006370"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="04912-104">notificar \_ atributo de sinalizador</span><span class="sxs-lookup"><span data-stu-id="04912-104">notify\_flag attribute</span></span>

<span data-ttu-id="04912-105">O atributo **\[ notificar \_ sinalizador \]** fornece uma notificação identificando se uma rotina de servidor é chamada.</span><span class="sxs-lookup"><span data-stu-id="04912-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="04912-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04912-107">*nome do procedimento*</span><span class="sxs-lookup"><span data-stu-id="04912-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="04912-108">Nome do procedimento remoto ao qual o procedimento do \_ sinalizador de notificação está associado.</span><span class="sxs-lookup"><span data-stu-id="04912-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04912-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="04912-109">Remarks</span></span>

<span data-ttu-id="04912-110">O atributo **\[ notificar \_ sinalizador \]** é semelhante ao uso para o atributo **\[ Notify \]** .</span><span class="sxs-lookup"><span data-stu-id="04912-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="04912-111">O nome do procedimento do **\[ \_ sinalizador \] de notificação** é o nome do procedimento remoto sufixado pelo **\_ \_ sinalizador Notify**.</span><span class="sxs-lookup"><span data-stu-id="04912-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="04912-112">O procedimento **\_ notificar \_ sinalizador** não requer nenhum parâmetro e não retorna um resultado.</span><span class="sxs-lookup"><span data-stu-id="04912-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="04912-113">Um protótipo desse procedimento também é gerado no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="04912-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="04912-114">Por exemplo, se o arquivo IDL contiver o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04912-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="04912-115">Especifique o seguinte no ACF para MIDL para gerar a chamada do **\_ \_ sinalizador Notify** :</span><span class="sxs-lookup"><span data-stu-id="04912-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="04912-116">O compilador MIDL gerará código stub de servidor que contém a seguinte chamada para o procedimento **\_ notificar \_ sinalizador** :</span><span class="sxs-lookup"><span data-stu-id="04912-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="04912-117">O arquivo de cabeçalho conterá um protótipo:</span><span class="sxs-lookup"><span data-stu-id="04912-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="04912-118">**\_ MIDL \_ NotifyFlag** será **true** se a rotina do servidor for chamada.</span><span class="sxs-lookup"><span data-stu-id="04912-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="04912-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04912-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="04912-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="04912-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04912-121">**sobre**</span><span class="sxs-lookup"><span data-stu-id="04912-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




