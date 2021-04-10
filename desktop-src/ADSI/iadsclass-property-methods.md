---
title: Métodos de propriedade IADsClass (IADs. h)
description: Os métodos de propriedade da interface IADsClass obtêm ou definem as propriedades a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsClass
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086047"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="48f16-105">Métodos de propriedade IADsClass</span><span class="sxs-lookup"><span data-stu-id="48f16-105">IADsClass Property Methods</span></span>

<span data-ttu-id="48f16-106">Os métodos de propriedade da interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) obtêm ou definem as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="48f16-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="48f16-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="48f16-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="48f16-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48f16-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="48f16-109">**Resumo**</span><span class="sxs-lookup"><span data-stu-id="48f16-109">**Abstract**</span></span>
<span data-ttu-id="48f16-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-111">Valor booliano que indica se essa classe é abstrata ou não abstrata.</span><span class="sxs-lookup"><span data-stu-id="48f16-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="48f16-112">Quando **true**, essa classe é uma classe abstrata e não pode ser instanciada diretamente no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="48f16-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="48f16-113">Classes abstratas só podem ser usadas como superclasses.</span><span class="sxs-lookup"><span data-stu-id="48f16-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="48f16-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-115">Tipo de dados de script: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48f16-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-116">**AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="48f16-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="48f16-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-118">Matriz de cadeias de caracteres ADsPath que indicam as classes superauxiliares das quais essa classe deriva.</span><span class="sxs-lookup"><span data-stu-id="48f16-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="48f16-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-120">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-121">**Auxiliar**</span><span class="sxs-lookup"><span data-stu-id="48f16-121">**Auxiliary**</span></span>
<span data-ttu-id="48f16-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-123">Valor booliano que indica se esta classe é auxiliar ou não.</span><span class="sxs-lookup"><span data-stu-id="48f16-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="48f16-124">Quando **true**, essa classe é uma classe auxiliar e não pode ser instanciada diretamente no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="48f16-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="48f16-125">As classes auxiliares só podem ser usadas como superclasses de outras classes auxiliares ou como uma fonte de propriedades adicionais em classes estruturais.</span><span class="sxs-lookup"><span data-stu-id="48f16-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="48f16-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-127">Tipo de dados de script: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48f16-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-128">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="48f16-128">**CLSID**</span></span>
<span data-ttu-id="48f16-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-130">CLSID opcional específico do provedor que identifica o objeto COM que implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="48f16-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="48f16-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-132">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="48f16-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-133">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="48f16-133">**Container**</span></span>
<span data-ttu-id="48f16-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-135">Valor booliano que indica se essa classe pode ser um contêiner de outras classes de objeto.</span><span class="sxs-lookup"><span data-stu-id="48f16-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="48f16-136">Se esse valor for **true**, você poderá chamar o método **Get \_ container** para obter uma matriz das classes de objeto que essa classe pode conter.</span><span class="sxs-lookup"><span data-stu-id="48f16-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="48f16-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-138">Tipo de dados de script: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48f16-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-139">**Contenção**</span><span class="sxs-lookup"><span data-stu-id="48f16-139">**Containment**</span></span>
<span data-ttu-id="48f16-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-141">Uma matriz **BSTR** na qual cada elemento é o nome de uma classe de objeto que essa classe pode conter.</span><span class="sxs-lookup"><span data-stu-id="48f16-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="48f16-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-143">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-144">**DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="48f16-144">**DerivedFrom**</span></span>
<span data-ttu-id="48f16-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-146">Matriz de cadeias de caracteres ADsPath que indicam as classes das quais essa classe foi derivada.</span><span class="sxs-lookup"><span data-stu-id="48f16-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="48f16-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-148">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-149">**HelpFileContext**</span><span class="sxs-lookup"><span data-stu-id="48f16-149">**HelpFileContext**</span></span>
<span data-ttu-id="48f16-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-151">ID de contexto dentro de **helpfilename** onde informações específicas para essa classe podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="48f16-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="48f16-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-153">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="48f16-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-154">**Arquivodeajudaname**</span><span class="sxs-lookup"><span data-stu-id="48f16-154">**HelpFileName**</span></span>
<span data-ttu-id="48f16-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-156">Nome de um arquivo de ajuda que contém mais informações sobre objetos desta classe.</span><span class="sxs-lookup"><span data-stu-id="48f16-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="48f16-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-158">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="48f16-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-159">**Obrigatórioproperties**</span><span class="sxs-lookup"><span data-stu-id="48f16-159">**MandatoryProperties**</span></span>
<span data-ttu-id="48f16-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-161">**SafeArray** de **Variant** s que lista as propriedades que devem ser definidas para essa classe a ser gravada no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="48f16-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="48f16-162">Se a classe contiver apenas uma propriedade, **obter \_ obrigatórioproperties** retornará um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="48f16-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="48f16-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-164">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-165">**Nome da nomenclatura**</span><span class="sxs-lookup"><span data-stu-id="48f16-165">**NamingProperties**</span></span>
<span data-ttu-id="48f16-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-167">**SafeArray** de **BSTR** s que lista as propriedades usadas para nomear atributos dessa classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="48f16-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="48f16-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-169">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-170">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="48f16-170">**OID**</span></span>
<span data-ttu-id="48f16-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-172">Identificador de objeto específico do provedor que define essa classe.</span><span class="sxs-lookup"><span data-stu-id="48f16-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="48f16-173">Isso é fornecido para permitir a extensão do esquema, usando Active Directory, em serviços de diretório que exigem OIDs específicos do provedor para classes.</span><span class="sxs-lookup"><span data-stu-id="48f16-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="48f16-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-175">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="48f16-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-176">**OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="48f16-176">**OptionalProperties**</span></span>
<span data-ttu-id="48f16-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-178">**SafeArray** de **Variant** s que lista as propriedades opcionais para esta classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="48f16-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="48f16-179">Se a classe contiver apenas uma propriedade, então, **obter \_ OptionalProperties** retornará um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="48f16-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="48f16-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-181">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-182">**PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="48f16-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="48f16-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-184">Matriz de cadeias de caracteres ADsPath que indicam as classes de esquema que podem conter instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="48f16-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="48f16-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48f16-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48f16-186">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="48f16-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48f16-187">**PrimaryInterface**</span><span class="sxs-lookup"><span data-stu-id="48f16-187">**PrimaryInterface**</span></span>
<span data-ttu-id="48f16-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48f16-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="48f16-189">GUID de identificador específico do provedor opcional que associa uma interface a objetos desta classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="48f16-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="48f16-190">Por exemplo, a classe "user" que dá suporte a [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) e **PrimaryInterface** é identificada pelo **IID \_ IADsUser**.</span><span class="sxs-lookup"><span data-stu-id="48f16-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="48f16-191">Isso deve estar no formato de cadeia de caracteres padrão de um GUID, conforme definido pelo COM.</span><span class="sxs-lookup"><span data-stu-id="48f16-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="48f16-192">Esse GUID é o valor que aparece na propriedade [**IADs:: get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) em instâncias dessa classe para provedores que implementam essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="48f16-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="48f16-193">A identificação de uma classe de esquema por IID da interface primária do código de classe permite o uso de **QueryInterface** em tempo de execução para determinar se um objeto é da classe desejada.</span><span class="sxs-lookup"><span data-stu-id="48f16-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="48f16-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48f16-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48f16-195">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="48f16-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="48f16-196">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48f16-196">Examples</span></span>

<span data-ttu-id="48f16-197">O exemplo de código a seguir mostra como usar a interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar se um objeto pode ser um contêiner e, em caso afirmativo, lista os nomes de quaisquer objetos contidos.</span><span class="sxs-lookup"><span data-stu-id="48f16-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="48f16-198">O exemplo de código a seguir mostra como usar a interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar se um objeto pode ser um contêiner e, em caso afirmativo, lista os nomes de quaisquer objetos contidos.</span><span class="sxs-lookup"><span data-stu-id="48f16-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="48f16-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48f16-199">Requirements</span></span>



| <span data-ttu-id="48f16-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="48f16-200">Requirement</span></span> | <span data-ttu-id="48f16-201">Valor</span><span class="sxs-lookup"><span data-stu-id="48f16-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48f16-202">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f16-202">Minimum supported client</span></span><br/> | <span data-ttu-id="48f16-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48f16-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48f16-204">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f16-204">Minimum supported server</span></span><br/> | <span data-ttu-id="48f16-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48f16-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48f16-206">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48f16-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f16-207"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f16-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="48f16-208">DLL</span><span class="sxs-lookup"><span data-stu-id="48f16-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48f16-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48f16-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="48f16-210">IID</span><span class="sxs-lookup"><span data-stu-id="48f16-210">IID</span></span><br/>                      | <span data-ttu-id="48f16-211">IID \_ IADsClass é definido como C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="48f16-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="48f16-212">Confira também</span><span class="sxs-lookup"><span data-stu-id="48f16-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f16-213">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="48f16-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="48f16-214">**IADsClass:: qualificadores**</span><span class="sxs-lookup"><span data-stu-id="48f16-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





