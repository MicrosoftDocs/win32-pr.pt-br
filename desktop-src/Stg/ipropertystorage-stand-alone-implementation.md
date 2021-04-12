---
title: Implementação IPropertyStorage-autônoma
description: A implementação autônoma fornecida pelo sistema do IPropertySetStorage inclui uma implementação de IPropertyStorage, a interface que lê e grava Propriedades em um armazenamento de conjunto de propriedades.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Implementação IPropertyStorage-autônoma
- IPropertyStorage Strctd STG, implementações, autônoma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366183"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="91bfc-105">Implementação IPropertyStorage-autônoma</span><span class="sxs-lookup"><span data-stu-id="91bfc-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="91bfc-106">A implementação autônoma fornecida pelo sistema do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) inclui uma implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), a interface que lê e grava Propriedades em um armazenamento de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="91bfc-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="91bfc-107">A interface **IPropertySetStorage** cria e abre conjuntos de propriedades em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="91bfc-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="91bfc-108">As interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) também são fornecidas na implementação autônoma.</span><span class="sxs-lookup"><span data-stu-id="91bfc-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="91bfc-109">Para obter um ponteiro para a implementação autônoma de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chame a função [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para criar um novo conjunto de propriedades ou [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obter o ponteiro de interface em um conjunto de propriedades existente (ou chamar os métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) da implementação autônoma [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).</span><span class="sxs-lookup"><span data-stu-id="91bfc-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="91bfc-110">A implementação autônoma do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) cria conjuntos de propriedades em qualquer objeto de armazenamento ou fluxo, não apenas em armazenamentos de arquivos compostos e fluxos.</span><span class="sxs-lookup"><span data-stu-id="91bfc-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="91bfc-111">A implementação autônoma não depende de arquivos compostos e pode ser usada com qualquer implementação de armazenamentos estruturados.</span><span class="sxs-lookup"><span data-stu-id="91bfc-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="91bfc-112">Para obter mais informações sobre a implementação de arquivo composto dessa interface, consulte [implementação de arquivo composto IPropertyStorage](ipropertystorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="91bfc-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="91bfc-113">Quando usar</span><span class="sxs-lookup"><span data-stu-id="91bfc-113">When to Use</span></span>

<span data-ttu-id="91bfc-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para gerenciar Propriedades em um único conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="91bfc-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="91bfc-115">Seus métodos dão suporte à leitura, gravação e exclusão de propriedades e aos nomes de cadeia de caracteres opcionais que podem ser associados a IDs de propriedade.</span><span class="sxs-lookup"><span data-stu-id="91bfc-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="91bfc-116">Outros métodos dão suporte às operações de confirmação e de reversão de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="91bfc-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="91bfc-117">Também há um método que define os horários associados ao armazenamento de propriedades e outro que permite que a atribuição de um CLSID seja usada para associar outro código, como o código de interface do usuário, com o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="91bfc-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="91bfc-118">O método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornece um ponteiro para a implementação autônoma de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que enumera as propriedades no conjunto.</span><span class="sxs-lookup"><span data-stu-id="91bfc-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="91bfc-119">Formatos de conjunto de propriedades versão 0 e versão 1</span><span class="sxs-lookup"><span data-stu-id="91bfc-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="91bfc-120">A implementação autônoma do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos formatos de serialização da versão 0 e do conjunto de propriedades da versão 1.</span><span class="sxs-lookup"><span data-stu-id="91bfc-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="91bfc-121">Para obter mais informações, consulte [serialização do conjunto de propriedades](version-0-vs--version-1-property-set-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="91bfc-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="91bfc-122">Os conjuntos de propriedades são criados no formato da versão 0 e permanecem nesse formato, a menos que novos recursos sejam solicitados.</span><span class="sxs-lookup"><span data-stu-id="91bfc-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="91bfc-123">Nesse momento, o formato é atualizado para a versão 1.</span><span class="sxs-lookup"><span data-stu-id="91bfc-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="91bfc-124">Por exemplo, se um conjunto de Propriedades for criado com o \_ sinalizador padrão PROPSETFLAG, seu formato será a versão 0.</span><span class="sxs-lookup"><span data-stu-id="91bfc-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="91bfc-125">Desde que os tipos de propriedade que estejam em conformidade com o formato da versão 0 sejam gravados e lidos a partir desse conjunto de propriedades, o conjunto de propriedades permanecerá no formato da versão 0.</span><span class="sxs-lookup"><span data-stu-id="91bfc-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="91bfc-126">Se um tipo de propriedade da versão 1 for gravado no conjunto de propriedades, o conjunto de propriedades será atualizado automaticamente para a versão 1.</span><span class="sxs-lookup"><span data-stu-id="91bfc-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="91bfc-127">Subsequentemente, esse conjunto de propriedades não pode mais ser lido por implementações que entendem apenas a versão 0.</span><span class="sxs-lookup"><span data-stu-id="91bfc-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="91bfc-128">Tipos de IPropertyStorage e variantes</span><span class="sxs-lookup"><span data-stu-id="91bfc-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="91bfc-129">A implementação autônoma de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) não dá suporte à expedição de tipos Variant VT \_ Unknown ou VT \_ no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="91bfc-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="91bfc-130">Os tipos variantes a seguir têm suporte em um SafeArray; ou seja, esses valores podem ser combinados com \_ a matriz VT no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="91bfc-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="91bfc-131">Tipos de variante com suporte em SafeArray por implementação de arquivo composto de [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="91bfc-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="91bfc-132">VT \_ i1</span><span class="sxs-lookup"><span data-stu-id="91bfc-132">VT\_I1</span></span>

<span data-ttu-id="91bfc-133">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="91bfc-133">VT\_UI1</span></span>

<span data-ttu-id="91bfc-134">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="91bfc-134">VT\_I2</span></span>

<span data-ttu-id="91bfc-135">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="91bfc-135">VT\_UI2</span></span>

<span data-ttu-id="91bfc-136">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="91bfc-136">VT\_I4</span></span>

<span data-ttu-id="91bfc-137">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="91bfc-137">VT\_UI4</span></span>

<span data-ttu-id="91bfc-138">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="91bfc-138">VT\_INT</span></span>

<span data-ttu-id="91bfc-139">VT \_ uint</span><span class="sxs-lookup"><span data-stu-id="91bfc-139">VT\_UINT</span></span>

<span data-ttu-id="91bfc-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="91bfc-140">VT\_R4</span></span>

<span data-ttu-id="91bfc-141">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="91bfc-141">VT\_R8</span></span>

<span data-ttu-id="91bfc-142">VT \_ Cy</span><span class="sxs-lookup"><span data-stu-id="91bfc-142">VT\_CY</span></span>

<span data-ttu-id="91bfc-143">Data de VT \_</span><span class="sxs-lookup"><span data-stu-id="91bfc-143">VT\_DATE</span></span>

<span data-ttu-id="91bfc-144">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="91bfc-144">VT\_BSTR</span></span>

<span data-ttu-id="91bfc-145">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="91bfc-145">VT\_BOOL</span></span>

<span data-ttu-id="91bfc-146">\_decimal VT</span><span class="sxs-lookup"><span data-stu-id="91bfc-146">VT\_DECIMAL</span></span>

<span data-ttu-id="91bfc-147">erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="91bfc-147">VT\_ERROR</span></span>

<span data-ttu-id="91bfc-148">variante do VT \_</span><span class="sxs-lookup"><span data-stu-id="91bfc-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="91bfc-149">Quando \_ a variante VT é combinada com \_ a matriz VT, o SAFEARRAY em si mantém as estruturas [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="91bfc-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="91bfc-150">No entanto, os tipos desses elementos devem ser extraídos da lista anterior, não pode ser VT \_ Variant e não podem incluir os \_ indicadores de vetor VT, VT \_ array ou VT \_ ByRef.</span><span class="sxs-lookup"><span data-stu-id="91bfc-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="91bfc-151">Métodos IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="91bfc-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="91bfc-152">A implementação autônoma do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="91bfc-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="91bfc-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="91bfc-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-154">Lê as propriedades especificadas na matriz *rgpspec* e fornece os valores de todas as propriedades válidas na matriz *rgVar* de elementos [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="91bfc-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="91bfc-155">Na implementação autônoma fornecida pelo sistema, os identificadores de propriedade duplicados que se referem aos tipos de fluxo/armazenamento resultam em várias chamadas para [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e o êxito ou a falha de [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depende da capacidade da implementação de armazenamento subjacente para compartilhar armazenamentos abertos.</span><span class="sxs-lookup"><span data-stu-id="91bfc-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="91bfc-156">Além disso, para garantir a operação thread-safe se a mesma propriedade com valor de fluxo ou de armazenamento for solicitada várias vezes pelo mesmo ponteiro [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , a abertura terá êxito ou falhará dependendo se a propriedade já estiver aberta e se o sistema de arquivos subjacente lida com várias aberturas de um fluxo ou armazenamento.</span><span class="sxs-lookup"><span data-stu-id="91bfc-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="91bfc-157">Assim, a operação [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) em uma propriedade com valor de fluxo ou de armazenamento sempre resulta em uma chamada para [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passando o acesso (STGM \_ ReadWrite, por exemplo) e valores de compartilhamento (STGM \_ compartilhamento \_ exclusivo, por exemplo) especificado quando o conjunto de propriedades foi originalmente aberto ou criado.</span><span class="sxs-lookup"><span data-stu-id="91bfc-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="91bfc-158">Se o método falhar, os valores gravados em *rgVar* \[ \] serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="91bfc-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="91bfc-159">Se algumas propriedades de fluxo ou de valor de armazenamento forem abertas com êxito, mas ocorrer um erro antes da execução ser concluída, essas propriedades deverão ser liberadas antes que o método seja retornado.</span><span class="sxs-lookup"><span data-stu-id="91bfc-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="91bfc-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-161">Grava as propriedades especificadas na matriz *rgpspec* \[ \] , atribuindo a elas as marcas e os valores de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificados em *rgVar* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="91bfc-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="91bfc-162">As propriedades que já existem são atribuídas aos valores **PROPVARIANT** especificados, e as propriedades que não existem atualmente são criadas.</span><span class="sxs-lookup"><span data-stu-id="91bfc-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="91bfc-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-164">Exclui as propriedades especificadas em *rgpspec* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="91bfc-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="91bfc-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-166">Lê os nomes de cadeia de caracteres existentes associados às IDs de propriedade especificadas na matriz *rgPropID* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="91bfc-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="91bfc-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-168">Atribui nomes de cadeia de caracteres especificados na matriz *rglpwstrName* às IDs de propriedade especificadas na matriz *rgPropID* .</span><span class="sxs-lookup"><span data-stu-id="91bfc-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="91bfc-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-170">Exclui os nomes de cadeia de caracteres das IDs de propriedade especificadas na matriz *rgPropID* gravando **NULL** no nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="91bfc-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="91bfc-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-172">Define o **CLSID** do fluxo do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="91bfc-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="91bfc-173">Na implementação autônoma, definir o CLSID em um conjunto de propriedades não simples (um que pode conter Propriedades com valor de armazenamento ou de fluxo, conforme descrito em [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) também define o CLSID no subarmazenamento subjacente para que ele possa ser obtido por meio de uma chamada para [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span><span class="sxs-lookup"><span data-stu-id="91bfc-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="91bfc-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-175">Para os conjuntos de propriedades simples e não simples, o libera a imagem de memória para o subsistema de disco.</span><span class="sxs-lookup"><span data-stu-id="91bfc-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="91bfc-176">Além disso, para conjuntos de propriedades de modo transacionado não simples, esse método chama [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="91bfc-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="91bfc-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-178">Somente para conjuntos de propriedades não simples, o chama o método [**REVERT**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) do armazenamento subjacente e reabre o fluxo ' Contents '.</span><span class="sxs-lookup"><span data-stu-id="91bfc-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="91bfc-179">Para conjuntos de propriedades simples, retorna apenas E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91bfc-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="91bfc-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-181">Cria um objeto enumerador que implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), os métodos que podem ser chamados para enumerar as estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que fornecem informações sobre cada uma das propriedades no conjunto.</span><span class="sxs-lookup"><span data-stu-id="91bfc-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="91bfc-182">Essa implementação cria uma matriz na qual o conjunto de propriedades inteiro é lido e que pode ser compartilhado quando [**IEnumSTATPROPSTG:: clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) é chamado.</span><span class="sxs-lookup"><span data-stu-id="91bfc-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="91bfc-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-184">Preenche os membros de uma estrutura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , que contém informações sobre o conjunto de propriedades como um todo.</span><span class="sxs-lookup"><span data-stu-id="91bfc-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="91bfc-185">No retorno, fornece um ponteiro para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="91bfc-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="91bfc-186">Para conjuntos de armazenamento não simples, essa implementação chama [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (ou [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) para obter as informações do armazenamento ou fluxo subjacente.</span><span class="sxs-lookup"><span data-stu-id="91bfc-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="91bfc-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="91bfc-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="91bfc-188">Somente para conjuntos de propriedades não simples, o define os tempos suportados pelo armazenamento subjacente.</span><span class="sxs-lookup"><span data-stu-id="91bfc-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="91bfc-189">Essa implementação de [**Settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chama o método [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) do armazenamento subjacente para modificar os horários.</span><span class="sxs-lookup"><span data-stu-id="91bfc-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="91bfc-190">Ele dá suporte às horas com suporte pelo método subjacente que pode ser tempo de modificação, hora de acesso ou hora de criação.</span><span class="sxs-lookup"><span data-stu-id="91bfc-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="91bfc-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91bfc-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91bfc-192">Implementação IPropertySetStorage-autônoma</span><span class="sxs-lookup"><span data-stu-id="91bfc-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="91bfc-193">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="91bfc-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="91bfc-194">**IStorage:: SetElementTimes**</span><span class="sxs-lookup"><span data-stu-id="91bfc-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="91bfc-195">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="91bfc-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="91bfc-196">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="91bfc-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="91bfc-197">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="91bfc-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 