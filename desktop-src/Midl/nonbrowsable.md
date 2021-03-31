---
title: atributo nonbrowsable
description: Use o atributo \ nonnavegável \ para marcar uma interface ou um membro de dispinterface que não deve ser exibido em um navegador de propriedades.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL de atributo não navegável
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917202"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="120b9-104">atributo nonbrowsable</span><span class="sxs-lookup"><span data-stu-id="120b9-104">nonbrowsable attribute</span></span>

<span data-ttu-id="120b9-105">Use o atributo **\[ nonnavegável \]** para marcar uma interface ou um membro de dispinterface que não deve ser exibido em um navegador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="120b9-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="120b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="120b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120b9-107">*Propriedade-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="120b9-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="120b9-108">Outros atributos que se aplicam à propriedade.</span><span class="sxs-lookup"><span data-stu-id="120b9-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="120b9-109">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="120b9-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="120b9-110">O tipo dos dados retornados pelo método.</span><span class="sxs-lookup"><span data-stu-id="120b9-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="120b9-111">*nome da propriedade*</span><span class="sxs-lookup"><span data-stu-id="120b9-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="120b9-112">O nome da propriedade ou do método.</span><span class="sxs-lookup"><span data-stu-id="120b9-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="120b9-113">*prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="120b9-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="120b9-114">Zero ou mais parâmetros a serem passados para o método.</span><span class="sxs-lookup"><span data-stu-id="120b9-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="120b9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="120b9-115">Remarks</span></span>

<span data-ttu-id="120b9-116">Determinadas propriedades não devem ser exibidas em um navegador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="120b9-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="120b9-117">Isso pode ser porque a recuperação do valor levaria muito tempo.</span><span class="sxs-lookup"><span data-stu-id="120b9-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="120b9-118">O exemplo impede que o usuário tente recuperar a propriedade *Count* , que retorna o número de linhas no dynaset. Esse número pode representar os resultados de uma consulta muito grande.</span><span class="sxs-lookup"><span data-stu-id="120b9-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="120b9-119">Outras propriedades podem ter efeitos inesperados no navegador.</span><span class="sxs-lookup"><span data-stu-id="120b9-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="120b9-120">Por exemplo, considere um controle com a propriedade "IsSelected" para informar se o controle está selecionado.</span><span class="sxs-lookup"><span data-stu-id="120b9-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="120b9-121">Se "IsSelected" for definido como false, um navegador de propriedades com base em seleção procurará um objeto diferente.</span><span class="sxs-lookup"><span data-stu-id="120b9-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="120b9-122">Observe que uma propriedade marcada como não **\[ navegável \]** ainda aparecerá em um pesquisador de objetos, que não mostra valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="120b9-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="120b9-123">Representação TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="120b9-123">Typeflag Representation</span></span>

<span data-ttu-id="120b9-124">A presença de FUNCFLAG \_ FNONBROWSABLE ou VARFLAG \_ FNONBROWSABLE.</span><span class="sxs-lookup"><span data-stu-id="120b9-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="120b9-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="120b9-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="120b9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="120b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120b9-127">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="120b9-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="120b9-128">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="120b9-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="120b9-129">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="120b9-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 