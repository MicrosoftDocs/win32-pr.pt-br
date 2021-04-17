---
description: Você pode usar os métodos e as propriedades do objeto SWbemObject para representar uma definição de classe de Instrumentação de Gerenciamento do Windows (WMI) ou uma instância de objeto.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Objeto SWbemObject (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813612"
---
# <a name="swbemobject-object"></a><span data-ttu-id="c877c-103">Objeto SWbemObject</span><span class="sxs-lookup"><span data-stu-id="c877c-103">SWbemObject object</span></span>

<span data-ttu-id="c877c-104">Você pode usar os métodos e as propriedades do objeto **SWbemObject** para representar uma definição de classe de instrumentação de gerenciamento do Windows (WMI) ou uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="c877c-105">Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c877c-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="c877c-106">Este objeto dá suporte a dois tipos de propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="c877c-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="c877c-107">Aqueles definidos nesta seção são propriedades genéricas e métodos que se aplicam a todos os objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="c877c-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="c877c-108">Além disso, esse objeto expõe as propriedades e os métodos do objeto subjacente como propriedades de automação dinâmica e métodos de **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="c877c-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="c877c-109">Os nomes e os tipos dessas propriedades e métodos dependem do objeto WMI subjacente.</span><span class="sxs-lookup"><span data-stu-id="c877c-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="c877c-110">Para obter mais informações sobre como esses métodos e propriedades dinâmicas são expostos, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="c877c-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="c877c-111">Da perspectiva do cliente WMI, esse objeto está sempre em processo.</span><span class="sxs-lookup"><span data-stu-id="c877c-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="c877c-112">As operações de gravação afetam apenas a cópia local do objeto e as operações de leitura sempre recuperam valores da cópia local.</span><span class="sxs-lookup"><span data-stu-id="c877c-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="c877c-113">As atualizações para o WMI são executadas somente quando objetos inteiros são gravados usando uma chamada para o método [**SWbemObject. put \_**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="c877c-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="c877c-114">Se você modificar as propriedades ou métodos em um objeto **SWbemObject** , suas alterações não serão gravadas no WMI até que você chame **SWbemObject \_ . put**.</span><span class="sxs-lookup"><span data-stu-id="c877c-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="c877c-115">O método genérico e os nomes de propriedade definidos nesta seção sempre terminam com um sublinhado à direita (" \_ ") para diferenciá-los dos métodos e propriedades dinâmicos do WMI do objeto subjacente.</span><span class="sxs-lookup"><span data-stu-id="c877c-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="c877c-116">Observe que **SWbemObject** não pode ser criado usando o VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Method.</span><span class="sxs-lookup"><span data-stu-id="c877c-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="c877c-117">Se você quiser criar uma nova classe vazia, use [**SWbemServices. Get**](swbemservices-get.md) com um parâmetro de caminho vazio.</span><span class="sxs-lookup"><span data-stu-id="c877c-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="c877c-118">Essa chamada retorna um objeto **SWbemObject** vazio que pode se tornar uma classe.</span><span class="sxs-lookup"><span data-stu-id="c877c-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="c877c-119">Em seguida, você pode fornecer um nome de classe para a propriedade de [**classe**](swbemobjectpath-class.md) do objeto [**SWbemObjectPath**](swbemobjectpath.md) retornado pela chamada de [**caminho \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="c877c-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="c877c-120">Adicione Propriedades à nova classe pelo método [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="c877c-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="c877c-121">Para criar uma instância, chame **GetObject** na nova classe.</span><span class="sxs-lookup"><span data-stu-id="c877c-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="c877c-122">O exemplo de código a seguir mostra como obter uma nova classe e adicionar uma propriedade a ela.</span><span class="sxs-lookup"><span data-stu-id="c877c-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="c877c-123">O objeto **SWbemObject** que representa a classe deve ser gravado no repositório WMI por uma chamada para [**Put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="c877c-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="c877c-124">Você pode examinar o repositório com uma ferramenta de exibição, como o [CIM Studio](further-information.md) , para verificar se a nova classe e a instância são exibidas.</span><span class="sxs-lookup"><span data-stu-id="c877c-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="c877c-125">Para obter um exemplo de como remover uma classe e uma instância do repositório, consulte [**SWbemServices. Delete**](swbemservices-delete.md) ou [**SWbemObject \_ . Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="c877c-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="c877c-126">Membros</span><span class="sxs-lookup"><span data-stu-id="c877c-126">Members</span></span>

<span data-ttu-id="c877c-127">O objeto **SWbemObject** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c877c-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="c877c-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="c877c-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="c877c-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c877c-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c877c-130">Métodos</span><span class="sxs-lookup"><span data-stu-id="c877c-130">Methods</span></span>

<span data-ttu-id="c877c-131">O objeto **SWbemObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c877c-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="c877c-132">Método</span><span class="sxs-lookup"><span data-stu-id="c877c-132">Method</span></span>                                                        | <span data-ttu-id="c877c-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="c877c-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c877c-134">**ASSOCIADORES\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="c877c-135">Recupera os associadores do objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="c877c-136">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="c877c-137">Recupera de forma assíncrona os associadores do objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="c877c-138">**8i\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="c877c-139">Faz uma cópia do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="c877c-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="c877c-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="c877c-141">Testa dois objetos para igualdade.</span><span class="sxs-lookup"><span data-stu-id="c877c-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="c877c-142">**Excluir\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="c877c-143">Exclui o objeto do WMI.</span><span class="sxs-lookup"><span data-stu-id="c877c-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="c877c-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="c877c-145">Exclui de forma assíncrona o objeto do WMI.</span><span class="sxs-lookup"><span data-stu-id="c877c-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="c877c-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="c877c-147">Executa um método exportado por um provedor de método.</span><span class="sxs-lookup"><span data-stu-id="c877c-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="c877c-148">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="c877c-149">Executa de forma assíncrona um método exportado por um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="c877c-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="c877c-150">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="c877c-151">Recupera a representação textual do objeto (sintaxe MOF).</span><span class="sxs-lookup"><span data-stu-id="c877c-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="c877c-152">**Instâncias\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="c877c-153">Retorna uma coleção de instâncias do objeto (que deve ser uma classe WMI).</span><span class="sxs-lookup"><span data-stu-id="c877c-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="c877c-154">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="c877c-155">De forma assíncrona retorna uma coleção de instâncias do objeto (que deve ser uma classe WMI).</span><span class="sxs-lookup"><span data-stu-id="c877c-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="c877c-156">**Posicione\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="c877c-157">Cria ou atualiza o objeto no WMI.</span><span class="sxs-lookup"><span data-stu-id="c877c-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="c877c-158">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="c877c-159">Cria ou atualiza de forma assíncrona o objeto no WMI.</span><span class="sxs-lookup"><span data-stu-id="c877c-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="c877c-160">**Referências\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="c877c-161">Retorna referências ao objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="c877c-162">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="c877c-163">De forma assíncrona retorna referências ao objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="c877c-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="c877c-165">Cria uma nova classe derivada do objeto atual (que deve ser uma classe WMI).</span><span class="sxs-lookup"><span data-stu-id="c877c-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="c877c-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="c877c-167">Cria uma nova instância do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="c877c-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="c877c-168">**Subclasses\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="c877c-169">Retorna uma coleção de subclasses do objeto (que deve ser uma classe WMI).</span><span class="sxs-lookup"><span data-stu-id="c877c-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="c877c-170">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="c877c-171">De forma assíncrona retorna uma coleção de subclasses do objeto (que deve ser uma classe WMI).</span><span class="sxs-lookup"><span data-stu-id="c877c-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c877c-172">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c877c-172">Properties</span></span>

<span data-ttu-id="c877c-173">O objeto **SWbemObject** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c877c-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="c877c-174">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c877c-174">Property</span></span>                                                   | <span data-ttu-id="c877c-175">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c877c-175">Access type</span></span>          | <span data-ttu-id="c877c-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="c877c-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c877c-177">**Derivação\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="c877c-178">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c877c-178">Read-only</span></span><br/> | <span data-ttu-id="c877c-179">Contém uma matriz de cadeias de caracteres que descreve a hierarquia de derivação para a classe.</span><span class="sxs-lookup"><span data-stu-id="c877c-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="c877c-180">**Métodos\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="c877c-181">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c877c-181">Read-only</span></span><br/> | <span data-ttu-id="c877c-182">Um objeto [**SWbemMethodSet**](swbemmethodset.md) que é a coleção de métodos para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="c877c-183">**Caminho\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="c877c-184">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c877c-184">Read-only</span></span><br/> | <span data-ttu-id="c877c-185">Contém um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="c877c-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="c877c-186">**Propriedades\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="c877c-187">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c877c-187">Read-only</span></span><br/> | <span data-ttu-id="c877c-188">Um objeto [**SWbemPropertySet**](swbempropertyset.md) que é a coleção de propriedades deste objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="c877c-189">**Qualificadores\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="c877c-190">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c877c-190">Read-only</span></span><br/> | <span data-ttu-id="c877c-191">Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que é a coleção de qualificadores para este objeto.</span><span class="sxs-lookup"><span data-stu-id="c877c-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="c877c-192">**Segurança\_**</span><span class="sxs-lookup"><span data-stu-id="c877c-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="c877c-193">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c877c-193">Read-only</span></span><br/> | <span data-ttu-id="c877c-194">Contém um objeto [**SWbemSecurity**](swbemsecurity.md) usado para ler ou alterar as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="c877c-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="c877c-195">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c877c-195">Examples</span></span>

<span data-ttu-id="c877c-196">A [lista de todas as propriedades e métodos de um](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) exemplo de código VBScript da classe WMI na galeria do TechNet usa o SWbemObject para listar todos os métodos e propriedades de uma classe WMI especificada.</span><span class="sxs-lookup"><span data-stu-id="c877c-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="c877c-197">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c877c-197">Requirements</span></span>



| <span data-ttu-id="c877c-198">Requisito</span><span class="sxs-lookup"><span data-stu-id="c877c-198">Requirement</span></span> | <span data-ttu-id="c877c-199">Valor</span><span class="sxs-lookup"><span data-stu-id="c877c-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c877c-200">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c877c-200">Minimum supported client</span></span><br/> | <span data-ttu-id="c877c-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c877c-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c877c-202">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c877c-202">Minimum supported server</span></span><br/> | <span data-ttu-id="c877c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c877c-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c877c-204">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c877c-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="c877c-205"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c877c-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c877c-206">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c877c-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="c877c-207"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c877c-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c877c-208">DLL</span><span class="sxs-lookup"><span data-stu-id="c877c-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c877c-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c877c-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c877c-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="c877c-210">CLSID</span></span><br/>                    | <span data-ttu-id="c877c-211">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="c877c-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c877c-212">IID</span><span class="sxs-lookup"><span data-stu-id="c877c-212">IID</span></span><br/>                      | <span data-ttu-id="c877c-213">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="c877c-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c877c-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="c877c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c877c-215">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="c877c-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="c877c-216">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="c877c-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

