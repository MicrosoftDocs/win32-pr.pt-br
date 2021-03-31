---
title: comm_status atributo
description: O atributo \ status de \ Comm \_ \ ACF faz com que um código de erro seja retornado quando ocorre um erro de comunicação durante a execução de uma função.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status do atributo MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638661"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="15762-104">atributo de status de comunicação \_</span><span class="sxs-lookup"><span data-stu-id="15762-104">comm\_status attribute</span></span>

<span data-ttu-id="15762-105">O atributo ACF de **\[ \_ status \] de comunicação** faz com que um código de erro seja retornado quando ocorre um erro de comunicação durante a execução de uma função.</span><span class="sxs-lookup"><span data-stu-id="15762-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="15762-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15762-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15762-107">*ACF-função-atributos*</span><span class="sxs-lookup"><span data-stu-id="15762-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="15762-108">Especifica zero ou mais atributos de função de ACF, como **\[ \_ status \] de comunicação** e **\[** [**Nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="15762-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="15762-109">Os atributos de função são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="15762-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="15762-110">Zero ou mais atributos podem ser aplicados a uma função.</span><span class="sxs-lookup"><span data-stu-id="15762-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="15762-111">Separe vários atributos de função com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="15762-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="15762-112">Observe que, se o **\[ \_ status \] de comunicação** aparecer como um atributo de função, ele também não poderá aparecer como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="15762-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="15762-113">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="15762-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="15762-114">Especifica o nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="15762-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="15762-115">*ACF-parâmetros-atributos*</span><span class="sxs-lookup"><span data-stu-id="15762-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="15762-116">Especifica os atributos que se aplicam a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="15762-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="15762-117">Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="15762-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="15762-118">Separe vários atributos de parâmetro com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="15762-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="15762-119">Os atributos de parâmetro são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="15762-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="15762-120">Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF.</span><span class="sxs-lookup"><span data-stu-id="15762-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="15762-121">Observe que, se o **\[ \_ status \] de comunicação** aparecer como um atributo de parâmetro, ele também não poderá aparecer como um atributo de função.</span><span class="sxs-lookup"><span data-stu-id="15762-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="15762-122">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="15762-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="15762-123">Especifica o parâmetro para a função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="15762-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="15762-124">Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="15762-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15762-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="15762-125">Remarks</span></span>

<span data-ttu-id="15762-126">O atributo de **\[ \_ status \] de comunicação** pode ser usado como um atributo de função ou como um atributo de parâmetro, mas pode aparecer apenas uma vez por função.</span><span class="sxs-lookup"><span data-stu-id="15762-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="15762-127">Ele pode ser aplicado à função ou a um parâmetro em cada função.</span><span class="sxs-lookup"><span data-stu-id="15762-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="15762-128">O atributo de **\[ \_ status \] de comm** pode ser aplicado somente a funções que retornam o tipo status de [**erro \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="15762-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="15762-129">Quando ocorre um erro de comunicação durante a execução da função, um código de erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="15762-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="15762-130">Quando o **\[ \_ status \] de comunicação** é usado como um atributo de parâmetro, o parâmetro deve ser definido no arquivo IDL e deve ser um **\[** parâmetro [**out**](out-idl.md) **\]** do tipo [**status de erro \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="15762-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="15762-131">Quando ocorre um erro de comunicação durante a execução da função, o parâmetro é definido como o código de erro.</span><span class="sxs-lookup"><span data-stu-id="15762-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="15762-132">Quando a chamada remota for concluída com êxito, o procedimento definirá o valor.</span><span class="sxs-lookup"><span data-stu-id="15762-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="15762-133">É possível que os atributos **\[ \_ \] status de comunicação** e **\[** [**\_ status de falha**](fault-status.md) sejam **\]** exibidos em uma única função, como atributos de função ou atributos de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="15762-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="15762-134">Se ambos os atributos forem atributos de função ou se se aplicarem ao mesmo parâmetro e nenhum erro ocorrer, a função ou o parâmetro terá o valor **status de erro \_ \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15762-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="15762-135">Caso contrário, ele conterá o valor de status de **\[ comunicação \_ \]** ou de **\[ \_ estado \] de falha** apropriado.</span><span class="sxs-lookup"><span data-stu-id="15762-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="15762-136">Como os valores retornados para o **\[ \_ status \] de comunicação** são diferentes dos valores retornados para o **\[ \_ status \] de falha**, os valores retornados são prontamente interpretados.</span><span class="sxs-lookup"><span data-stu-id="15762-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="15762-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="15762-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15762-138">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="15762-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="15762-139">**status de erro \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="15762-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="15762-140">**status de falha \_**</span><span class="sxs-lookup"><span data-stu-id="15762-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="15762-141">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="15762-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="15762-142">**fora**</span><span class="sxs-lookup"><span data-stu-id="15762-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




