---
description: Define os parâmetros de entrada e saída para métodos.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Classe __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813295"
---
# <a name="__parameters-class"></a><span data-ttu-id="42df8-103">\_\_Classe Parameters</span><span class="sxs-lookup"><span data-stu-id="42df8-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="42df8-104">A classe de sistema **\_ \_ Parameters** é uma classe abstrata que define os parâmetros de entrada e saída para métodos.</span><span class="sxs-lookup"><span data-stu-id="42df8-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="42df8-105">Ele também é usado para passar valores de parâmetros de entrada e saída entre um cliente WMI e um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="42df8-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="42df8-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="42df8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="42df8-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="42df8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="42df8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42df8-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="42df8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="42df8-109">Members</span></span>

<span data-ttu-id="42df8-110">A classe **\_ \_ Parameters** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="42df8-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="42df8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="42df8-111">Remarks</span></span>

<span data-ttu-id="42df8-112">Para definir um método em uma classe de usuário, um cliente WMI cria uma cópia da classe **\_ \_ Parameters** e adiciona uma propriedade para cada parâmetro de entrada em um método.</span><span class="sxs-lookup"><span data-stu-id="42df8-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="42df8-113">Se o método contiver um valor de retorno ou parâmetros de saída, outra cópia dos **\_ \_ parâmetros** deverá ser criada.</span><span class="sxs-lookup"><span data-stu-id="42df8-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="42df8-114">Se o método retornar um valor de retorno, o cliente deverá adicionar uma propriedade chamada **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="42df8-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="42df8-115">O provedor de método, em seguida, armazena os parâmetros do método com uma chamada para [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="42df8-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="42df8-116">Para invocar um método, um cliente chama o seguinte em sequência:</span><span class="sxs-lookup"><span data-stu-id="42df8-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="42df8-117">[**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar uma cópia da classe **\_ \_ Parameters** que é armazenada por [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="42df8-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="42df8-118">[**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)e, em seguida, define uma propriedade para cada parâmetro de entrada para o método.</span><span class="sxs-lookup"><span data-stu-id="42df8-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="42df8-119">[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para executar o método.</span><span class="sxs-lookup"><span data-stu-id="42df8-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="42df8-120">Depois que o método terminar a execução, outra instância de classe de **\_ \_ parâmetros** poderá ser retornada se o método tiver parâmetros de saída ou um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="42df8-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="42df8-121">Se o método foi invocado usando [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), a instância de **\_ \_ parâmetros** é retornada como um argumento de saída.</span><span class="sxs-lookup"><span data-stu-id="42df8-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="42df8-122">Se o método foi invocado usando [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), a instância de **\_ \_ parâmetros** será retornada como um parâmetro para [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="42df8-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="42df8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42df8-123">Requirements</span></span>



| <span data-ttu-id="42df8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42df8-124">Requirement</span></span> | <span data-ttu-id="42df8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="42df8-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="42df8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42df8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42df8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42df8-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="42df8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42df8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42df8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42df8-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="42df8-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="42df8-130">Namespace</span></span><br/>                | <span data-ttu-id="42df8-131">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="42df8-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="42df8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="42df8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42df8-133">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="42df8-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="42df8-134">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="42df8-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="42df8-135">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="42df8-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




