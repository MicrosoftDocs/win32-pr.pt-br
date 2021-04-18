---
description: Usado para relatar informações detalhadas sobre o status e o erro.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Classe __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787639"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="77423-103">\_\_Classe ExtendedStatus</span><span class="sxs-lookup"><span data-stu-id="77423-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="77423-104">A classe de sistema **\_ \_ ExtendedStatus** é usada para relatar informações detalhadas de status e erro.</span><span class="sxs-lookup"><span data-stu-id="77423-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="77423-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="77423-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="77423-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="77423-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="77423-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77423-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="77423-108">Membros</span><span class="sxs-lookup"><span data-stu-id="77423-108">Members</span></span>

<span data-ttu-id="77423-109">A classe **\_ \_ ExtendedStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="77423-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="77423-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77423-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77423-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77423-111">Properties</span></span>

<span data-ttu-id="77423-112">A classe **\_ \_ ExtendedStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="77423-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77423-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="77423-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77423-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77423-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77423-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77423-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77423-116">Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.</span><span class="sxs-lookup"><span data-stu-id="77423-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="77423-117">**Operação**</span><span class="sxs-lookup"><span data-stu-id="77423-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77423-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77423-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77423-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77423-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77423-120">Operação que ocorre no momento de uma falha ou anomalia.</span><span class="sxs-lookup"><span data-stu-id="77423-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="77423-121">Normalmente, Instrumentação de Gerenciamento do Windows (WMI) define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="77423-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="77423-122">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="77423-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77423-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77423-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77423-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77423-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77423-125">Parâmetros envolvidos em um erro ou alteração de status.</span><span class="sxs-lookup"><span data-stu-id="77423-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="77423-126">Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.</span><span class="sxs-lookup"><span data-stu-id="77423-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="77423-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="77423-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77423-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77423-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77423-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77423-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77423-130">Identifica o provedor que causa ou relata um erro ou uma alteração de status.</span><span class="sxs-lookup"><span data-stu-id="77423-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="77423-131">Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "Gerenciamento do Windows".</span><span class="sxs-lookup"><span data-stu-id="77423-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="77423-132">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="77423-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77423-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77423-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77423-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77423-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77423-135">Contém um código de erro ou informações para uma operação.</span><span class="sxs-lookup"><span data-stu-id="77423-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="77423-136">Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="77423-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="77423-137">Essa propriedade é herdada de [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="77423-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77423-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="77423-138">Remarks</span></span>

<span data-ttu-id="77423-139">A classe **\_ \_ ExtendedStatus** é derivada da classe [**\_ \_ NotifyStatus**](--notifystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="77423-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="77423-140">Use a classe **\_ \_ ExtendedStatus** para relatar informações mais complexas do que um código de resultado simples.</span><span class="sxs-lookup"><span data-stu-id="77423-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="77423-141">Os provedores podem derivar suas próprias classes de **\_ \_ ExtendedStatus** se exigirem mais propriedades para descrever os erros.</span><span class="sxs-lookup"><span data-stu-id="77423-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="77423-142">A propriedade **StatusCode** , herdada da classe pai [**\_ \_ NotifyStatus**](--notifystatus.md) , é um inteiro sem sinal que representa o erro ou o valor de status.</span><span class="sxs-lookup"><span data-stu-id="77423-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="77423-143">Quando as instâncias dessa classe são retornadas de um método por um provedor dinâmico, as propriedades **StatusCode** e **Description** são definidas pelo provedor e as outras propriedades são definidas pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="77423-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="77423-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77423-144">Examples</span></span>

<span data-ttu-id="77423-145">O exemplo de código a seguir, extraído do [FND: como tratar Configuration Manager erros assíncronos usando](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) o exemplo de código do WMI VBScript na galeria do TechNet, descreve como usar o **\_ \_ ExtendedStatus** para recuperar informações de erro.</span><span class="sxs-lookup"><span data-stu-id="77423-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="77423-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77423-146">Requirements</span></span>



| <span data-ttu-id="77423-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="77423-147">Requirement</span></span> | <span data-ttu-id="77423-148">Valor</span><span class="sxs-lookup"><span data-stu-id="77423-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="77423-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77423-149">Minimum supported client</span></span><br/> | <span data-ttu-id="77423-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77423-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="77423-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77423-151">Minimum supported server</span></span><br/> | <span data-ttu-id="77423-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77423-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="77423-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="77423-153">Namespace</span></span><br/>                | <span data-ttu-id="77423-154">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="77423-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="77423-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="77423-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77423-156">**\_\_NotifyStatus**</span><span class="sxs-lookup"><span data-stu-id="77423-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="77423-157">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="77423-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

