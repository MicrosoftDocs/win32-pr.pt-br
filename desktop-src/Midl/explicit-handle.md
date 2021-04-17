---
title: explicit_handle atributo
description: O atributo \ \_ identificador \ explícito \ ACF especifica que cada procedimento tem, como seu primeiro parâmetro, um identificador primitivo, como um tipo de manipulador \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle do atributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105748171"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="455be-104">\_atributo de identificador explícito</span><span class="sxs-lookup"><span data-stu-id="455be-104">explicit\_handle attribute</span></span>

<span data-ttu-id="455be-105">O \[ atributo de ACF **\_ identificador explícito** \] especifica que cada procedimento tem, como seu primeiro parâmetro, um identificador primitivo, como um tipo de [**manipulador \_ t**](handle-t.md) .</span><span class="sxs-lookup"><span data-stu-id="455be-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="455be-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="455be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="455be-107">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="455be-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="455be-108">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="455be-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="455be-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="455be-109">Remarks</span></span>

<span data-ttu-id="455be-110">Quando você usa o atributo **\[ \_ identificador \] explícito** , cada procedimento tem um identificador primitivo como seu primeiro parâmetro, mesmo que o arquivo IDL não contenha esse identificador em sua lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="455be-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="455be-111">Os protótipos emitidos para o arquivo de cabeçalho e rotinas de stub contêm o parâmetro adicional, e esse parâmetro é usado como o identificador para direcionar a chamada remota.</span><span class="sxs-lookup"><span data-stu-id="455be-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="455be-112">O atributo **\[ \_ identificador \] explícito** afeta os procedimentos remotos e os procedimentos de serialização.</span><span class="sxs-lookup"><span data-stu-id="455be-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="455be-113">Para a serialização de tipo, as rotinas de suporte são geradas com o parâmetro inicial como um identificador explícito (serialização).</span><span class="sxs-lookup"><span data-stu-id="455be-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="455be-114">Se o atributo **\[ \_ identificador \] explícito** não for usado, o aplicativo ainda poderá especificar que uma operação tenha um identificador explícito (associação ou serialização) direcionando a chamada.</span><span class="sxs-lookup"><span data-stu-id="455be-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="455be-115">Para fazer isso, um protótipo com um argumento contendo um tipo de identificador é fornecido para o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="455be-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="455be-116">Observe que, no modo padrão, um argumento que não aparece primeiro também pode ser usado como um identificador que direciona a chamada.</span><span class="sxs-lookup"><span data-stu-id="455be-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="455be-117">Portanto, embora o atributo **\[ \_ identificador \] explícito** seja uma maneira de dar ao protótipo IDL um atributo de **\[ \_ identificador \] explícito** primitivo, ele não requer necessariamente uma alteração no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="455be-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="455be-118">No modo [**/OSF**](-osf.md) , somente o primeiro argumento pode ser usado como um tipo de identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="455be-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="455be-119">O atributo **\[ \_ identificador \] explícito** pode ser usado como um atributo de interface ou um atributo de operação.</span><span class="sxs-lookup"><span data-stu-id="455be-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="455be-120">Como um atributo de interface, ele afeta todas as operações na interface e todos os tipos que exigem suporte de serialização.</span><span class="sxs-lookup"><span data-stu-id="455be-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="455be-121">No entanto, se ele for usado como um atributo de operação, ele afetará apenas essa operação específica.</span><span class="sxs-lookup"><span data-stu-id="455be-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="455be-122">Se um método contiver um ou \[ mais \] identificadores de contexto, o mais à esquerda \[ no \] identificador de contexto será usado como o identificador de associação e nenhum identificador explícito adicional será criado.</span><span class="sxs-lookup"><span data-stu-id="455be-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="455be-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="455be-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="455be-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="455be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455be-125">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="455be-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="455be-126">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="455be-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="455be-127">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="455be-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="455be-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="455be-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




