---
title: fault_status atributo
description: O atributo \ \_ status de falha \ ACF especifica que um código de erro de tipo status de erro \_ \_ t indica uma falha do procedimento remoto, em vez de outros tipos de problemas, como erros de comunicação.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status do atributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638427"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="cbf89-104">atributo de status de falha \_</span><span class="sxs-lookup"><span data-stu-id="cbf89-104">fault\_status attribute</span></span>

<span data-ttu-id="cbf89-105">O atributo ACF de **\[ \_ status \] de falha** especifica que um código de erro de tipo status de [**erro \_ \_ t**](error-status-t.md) indica uma falha do procedimento remoto, em vez de outros tipos de problemas, como erros de comunicação.</span><span class="sxs-lookup"><span data-stu-id="cbf89-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="cbf89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbf89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf89-107">*ACF-função-atributos*</span><span class="sxs-lookup"><span data-stu-id="cbf89-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf89-108">Especifica zero ou mais atributos de função de ACF, como **\[ \_ status \] de falha** e **\[** [**Nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="cbf89-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="cbf89-109">Os atributos de função são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="cbf89-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="cbf89-110">Observe que zero ou mais atributos podem ser aplicados a uma função.</span><span class="sxs-lookup"><span data-stu-id="cbf89-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="cbf89-111">Separe vários atributos de função com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="cbf89-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="cbf89-112">Observe também que, se o **\[ \_ status \] de falha** aparecer como um atributo de função, ele também não poderá aparecer como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cbf89-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="cbf89-113">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="cbf89-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf89-114">Especifica o nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cbf89-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="cbf89-115">*ACF-parâmetros-atributos*</span><span class="sxs-lookup"><span data-stu-id="cbf89-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf89-116">Especifica os atributos que se aplicam a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cbf89-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="cbf89-117">Observe que zero ou mais atributos podem ser aplicados ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cbf89-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="cbf89-118">Os atributos de parâmetro são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="cbf89-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="cbf89-119">Separe vários atributos de parâmetro com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="cbf89-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="cbf89-120">Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF.</span><span class="sxs-lookup"><span data-stu-id="cbf89-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="cbf89-121">Observe que, se o **\[ \_ status \] de falha** aparecer como um atributo de parâmetro, ele também não poderá aparecer como um atributo de função.</span><span class="sxs-lookup"><span data-stu-id="cbf89-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="cbf89-122">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="cbf89-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf89-123">Especifica o parâmetro para a função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cbf89-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="cbf89-124">Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cbf89-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbf89-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbf89-125">Remarks</span></span>

<span data-ttu-id="cbf89-126">O atributo **\[ \_ status \] de falha** pode ser usado como um atributo de função ou como um atributo de parâmetro, mas pode aparecer apenas uma vez por função.</span><span class="sxs-lookup"><span data-stu-id="cbf89-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="cbf89-127">Ele pode ser aplicado à própria função ou a um parâmetro em cada função.</span><span class="sxs-lookup"><span data-stu-id="cbf89-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="cbf89-128">O atributo **\[ \_ status \] de falha** pode ser aplicado somente a funções que retornam o tipo status de [**erro \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="cbf89-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="cbf89-129">Quando o procedimento remoto falha de forma que faz com que uma PDU de falha seja retornada, um código de erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="cbf89-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="cbf89-130">Quando o **\[ \_ status \] de falha** é usado como um atributo de parâmetro, o parâmetro deve ser um **\[** parâmetro [**out**](out-idl.md) **\]** do tipo [**status de erro \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="cbf89-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="cbf89-131">Se ocorrer um erro de servidor, o parâmetro será definido como o código de erro.</span><span class="sxs-lookup"><span data-stu-id="cbf89-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="cbf89-132">Quando a chamada remota for concluída com êxito, o procedimento definirá o valor.</span><span class="sxs-lookup"><span data-stu-id="cbf89-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="cbf89-133">O parâmetro associado ao atributo **\[ \_ status \] de falha** não precisa ser especificado no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cbf89-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="cbf89-134">Quando o parâmetro não é especificado, um novo parâmetro [**out**](out-idl.md) do tipo [**status de erro \_ \_ t**](error-status-t.md) é gerado após o último parâmetro definido no arquivo IDL do DCE.</span><span class="sxs-lookup"><span data-stu-id="cbf89-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="cbf89-135">É possível que os atributos **\[ \_ \] status de falha** e **\[** [**\_ status de comunicação**](comm-status.md) **\]** apareçam em uma única função, seja como atributos de função ou atributos de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cbf89-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="cbf89-136">Se ambos os atributos forem atributos de função ou se se aplicarem ao mesmo parâmetro e nenhum erro ocorrer, a função ou o parâmetro terá o valor **status de erro \_ \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cbf89-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="cbf89-137">Caso contrário, ele contém o valor de código de status apropriado.</span><span class="sxs-lookup"><span data-stu-id="cbf89-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="cbf89-138">Como os valores retornados para o **\[ \_ status \] de falha** são diferentes dos valores retornados para o **\[ \_ status \] de comunicação**, os valores retornados são prontamente interpretados.</span><span class="sxs-lookup"><span data-stu-id="cbf89-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbf89-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cbf89-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf89-140">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="cbf89-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="cbf89-141">**status de comunicação \_**</span><span class="sxs-lookup"><span data-stu-id="cbf89-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="cbf89-142">**status de erro \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="cbf89-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="cbf89-143">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="cbf89-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="cbf89-144">**fora**</span><span class="sxs-lookup"><span data-stu-id="cbf89-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




