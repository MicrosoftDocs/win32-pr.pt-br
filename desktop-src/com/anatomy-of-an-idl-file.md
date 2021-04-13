---
title: Anatomia de um arquivo IDL
description: Esses arquivos IDL de exemplo demonstram as construções fundamentais da definição de interface.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104297851"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="e50f3-103">Anatomia de um arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="e50f3-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="e50f3-104">Esses arquivos IDL de exemplo demonstram as construções fundamentais da definição de interface.</span><span class="sxs-lookup"><span data-stu-id="e50f3-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="e50f3-105">Alocação de memória, marshaling personalizado e mensagens assíncronas são apenas alguns dos recursos que podem ser implementados em uma interface COM personalizada.</span><span class="sxs-lookup"><span data-stu-id="e50f3-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="e50f3-106">Os atributos MIDL são usados para definir interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="e50f3-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="e50f3-107">Para obter mais informações sobre como implementar interfaces e bibliotecas de tipos, incluindo um resumo de atributos MIDL, consulte [definições de interface e bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries) no guia e referência do programador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="e50f3-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="e50f3-108">Para obter uma referência completa de todos os atributos de MIDL, palavras-chave e diretivas, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="e50f3-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="e50f3-109">Exemplo de IDL</span><span class="sxs-lookup"><span data-stu-id="e50f3-109">Example.idl</span></span>

<span data-ttu-id="e50f3-110">O arquivo IDL de exemplo a seguir define duas interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="e50f3-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="e50f3-111">Nesse arquivo IDL, Midl.exe gerará proxy/stub e arquivos de cabeçalho e código de marshaling.</span><span class="sxs-lookup"><span data-stu-id="e50f3-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="e50f3-112">Uma desseção linha por linha segue o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e50f3-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="e50f3-113">A instrução de [**importação**](/windows/desktop/Midl/import) de IDL é usada aqui para trazer um arquivo de cabeçalho, Mydefs. h, que contém tipos definidos pelo usuário e Unknwn. idl, que contém a definição de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), da qual IFace1 e IFace2 derivam.</span><span class="sxs-lookup"><span data-stu-id="e50f3-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="e50f3-114">O atributo [**Object**](/windows/desktop/Midl/object) identifica a interface como uma interface de objeto e informa ao compilador MIDL para gerar código de proxy/stub em vez de stubs de cliente e de servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="e50f3-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="e50f3-115">Os métodos de interface de objeto devem ter um tipo de retorno de [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), para permitir que o mecanismo RPC subjacente Relate erros para chamadas que não foram concluídas devido a problemas de rede.</span><span class="sxs-lookup"><span data-stu-id="e50f3-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="e50f3-116">O atributo [**UUID**](/windows/desktop/Midl/uuid) especifica o identificador de interface (IID).</span><span class="sxs-lookup"><span data-stu-id="e50f3-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="e50f3-117">Cada interface, classe e biblioteca de tipos deve ser identificada com seu próprio identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e50f3-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="e50f3-118">Use o Uuidgen.exe do utilitário para gerar um conjunto de IDs exclusivos para suas interfaces e outros componentes.</span><span class="sxs-lookup"><span data-stu-id="e50f3-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="e50f3-119">A palavra-chave [**interface**](/windows/desktop/Midl/interface) define o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="e50f3-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="e50f3-120">Todas as interfaces de objeto devem derivar, direta ou indiretamente, de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="e50f3-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="e50f3-121">O [**parâmetro direcional especifica**](/windows/desktop/Midl/in) um parâmetro que é definido somente pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e50f3-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="e50f3-122">O parâmetro [**out**](/windows/desktop/Midl/out-idl) especifica os dados que são passados de volta para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e50f3-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="e50f3-123">O uso de ambos os atributos direcionais em um parâmetro especifica que o parâmetro é usado para enviar dados para o método e para passar dados de volta para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e50f3-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="e50f3-124">O [**atributo \_ padrão de ponteiro**](/windows/desktop/Midl/pointer-default) especifica o tipo de ponteiro padrão ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)ou [**PTR**](/windows/desktop/Midl/ptr)) para todos os ponteiros, exceto aqueles incluídos nas listas de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e50f3-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="e50f3-125">Se nenhum tipo padrão for especificado, MIDL assumirá que ponteiros únicos são **exclusivos**.</span><span class="sxs-lookup"><span data-stu-id="e50f3-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="e50f3-126">No entanto, quando você tem vários níveis de ponteiros, deve especificar explicitamente um tipo de ponteiro padrão, mesmo se desejar que o tipo padrão seja **exclusivo**.</span><span class="sxs-lookup"><span data-stu-id="e50f3-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="e50f3-127">No exemplo anterior, a matriz BkfstStuff \[ \] é uma *matriz compatível*, cujo tamanho é determinado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e50f3-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="e50f3-128">O atributo [**Max \_ is**](/windows/desktop/Midl/max-is) especifica a variável que contém o valor máximo para o índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="e50f3-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="e50f3-129">O atributo [**Size \_ também é**](/windows/desktop/Midl/size-is) usado para especificar o tamanho de uma matriz ou, como no exemplo anterior, vários níveis de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="e50f3-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="e50f3-130">No exemplo, a chamada pode ser feita sem saber com antecedência a quantidade de dados que será retornada.</span><span class="sxs-lookup"><span data-stu-id="e50f3-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="e50f3-131">Example2. idl</span><span class="sxs-lookup"><span data-stu-id="e50f3-131">Example2.idl</span></span>

<span data-ttu-id="e50f3-132">O exemplo de IDL a seguir (que reutiliza as interfaces descritas no exemplo de IDL anterior) mostra as várias maneiras de gerar informações de biblioteca de tipos para interfaces.</span><span class="sxs-lookup"><span data-stu-id="e50f3-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="e50f3-133">O atributo [**HelpString**](/windows/desktop/Midl/helpstring) é opcional; Você o usa para descrever brevemente o objeto ou para fornecer uma linha de status.</span><span class="sxs-lookup"><span data-stu-id="e50f3-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="e50f3-134">Essas cadeias de caracteres de ajuda são legíveis com um pesquisador de objetos, como aquele fornecido com o Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e50f3-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="e50f3-135">O atributo [**Dual**](/windows/desktop/Midl/dual) no IFace3 cria uma interface que é uma interface de expedição e uma interface com.</span><span class="sxs-lookup"><span data-stu-id="e50f3-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="e50f3-136">Como ele é derivado de **IDispatch**, uma interface dupla dá suporte à automação, que é o que o atributo [**oleautomation**](/windows/desktop/Midl/oleautomation) especifica.</span><span class="sxs-lookup"><span data-stu-id="e50f3-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="e50f3-137">IFace3 importa Oaidl. idl para obter a definição de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="e50f3-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="e50f3-138">A instrução [**library**](/windows/desktop/Midl/library) define a biblioteca de tipos ExampleLib, que tem seus próprios atributos [**UUID**](/windows/desktop/Midl/uuid), [**HelpString**](/windows/desktop/Midl/helpstring)e [**version**](/windows/desktop/Midl/version) .</span><span class="sxs-lookup"><span data-stu-id="e50f3-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="e50f3-139">Dentro da definição da biblioteca de tipos, a diretiva [**importlib**](/windows/desktop/Midl/importlib) coloca em uma biblioteca de tipos compilada.</span><span class="sxs-lookup"><span data-stu-id="e50f3-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="e50f3-140">Todas as definições de biblioteca de tipos devem trazer a biblioteca de tipos base definida em Stdole32. tlb.</span><span class="sxs-lookup"><span data-stu-id="e50f3-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="e50f3-141">Essa definição de biblioteca de tipos demonstra três maneiras diferentes de incluir interfaces na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="e50f3-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="e50f3-142">IFace3 é incluído meramente referenciando-o dentro da instrução da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e50f3-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="e50f3-143">A instrução [**coclass**](/windows/desktop/Midl/coclass) define uma classe de componente totalmente nova, BkfstComponent, que inclui duas interfaces definidas anteriormente, IFace1 e IFace2.</span><span class="sxs-lookup"><span data-stu-id="e50f3-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="e50f3-144">O atributo padrão designa IFace1 como a interface padrão.</span><span class="sxs-lookup"><span data-stu-id="e50f3-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="e50f3-145">IFace4 é descrito dentro da instrução de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e50f3-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="e50f3-146">O atributo [**propput**](/windows/desktop/Midl/propput) em methoded indica que o método executa uma ação set em uma propriedade de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="e50f3-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="e50f3-147">O atributo [**propget**](/windows/desktop/Midl/propget) indica que o método recupera informações de uma propriedade de mesmo nome que o método.</span><span class="sxs-lookup"><span data-stu-id="e50f3-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="e50f3-148">O atributo [**retval**](/windows/desktop/Midl/retval) em methoded designa um parâmetro de saída que contém o valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="e50f3-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
