---
description: O método LoadXML carrega dados de propriedade expressos em linguagem XML (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Método IPropertySetter:: LoadXML (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754241"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="bc563-103">Método IPropertySetter:: LoadXML</span><span class="sxs-lookup"><span data-stu-id="bc563-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="bc563-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="bc563-104">\[Deprecated.</span></span> <span data-ttu-id="bc563-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc563-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bc563-106">O `LoadXML` método carrega dados de propriedade expressos em linguagem XML (XML).</span><span class="sxs-lookup"><span data-stu-id="bc563-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc563-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc563-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="bc563-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc563-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc563-109">*PXML* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc563-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc563-110">Ponteiro para a interface **IUnknown** de um elemento XML criado pelo Microsoft XML Parser.</span><span class="sxs-lookup"><span data-stu-id="bc563-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc563-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc563-111">Return value</span></span>

<span data-ttu-id="bc563-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc563-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bc563-113">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="bc563-113">Possible values include the following.</span></span>



| <span data-ttu-id="bc563-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bc563-114">Return code</span></span>                                                                                                  | <span data-ttu-id="bc563-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc563-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="bc563-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="bc563-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="bc563-117">Nenhum dado de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bc563-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="bc563-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bc563-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="bc563-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bc563-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="bc563-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bc563-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="bc563-121">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="bc563-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="bc563-122"><dt>**VFW \_ E \_ \_ formato de arquivo inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc563-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="bc563-123">Formato inválido.</span><span class="sxs-lookup"><span data-stu-id="bc563-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="bc563-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc563-124">Remarks</span></span>

<span data-ttu-id="bc563-125">Normalmente, os aplicativos não precisarão usar esse método.</span><span class="sxs-lookup"><span data-stu-id="bc563-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="bc563-126">O DES o usa internamente para carregar Propriedades de arquivos XTL.</span><span class="sxs-lookup"><span data-stu-id="bc563-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="bc563-127">Para usar esse método, crie um objeto **IXMLDocument** e use-o para analisar um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="bc563-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="bc563-128">Em seguida, use o objeto **IXMLDocument** para recuperar objetos **IXMLElement** .</span><span class="sxs-lookup"><span data-stu-id="bc563-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="bc563-129">Se o objeto tiver Propriedades, você poderá passar o ponteiro **IXMLElement** para o método **LoadXml** .</span><span class="sxs-lookup"><span data-stu-id="bc563-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="bc563-130">O método carrega as propriedades no setter da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bc563-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="bc563-131">As interfaces **IXMLDocument** e **IXMLElement** são implementadas no Microsoft XML Core Services (MSXML) versão 1,0, mas não são implementadas em versões mais recentes do MSXML.</span><span class="sxs-lookup"><span data-stu-id="bc563-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="bc563-132">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="bc563-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bc563-133">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bc563-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bc563-134">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bc563-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc563-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc563-135">Requirements</span></span>



| <span data-ttu-id="bc563-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc563-136">Requirement</span></span> | <span data-ttu-id="bc563-137">Valor</span><span class="sxs-lookup"><span data-stu-id="bc563-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc563-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc563-138">Header</span></span><br/>  | <dl> <span data-ttu-id="bc563-139"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc563-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bc563-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc563-140">Library</span></span><br/> | <dl> <span data-ttu-id="bc563-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc563-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc563-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc563-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc563-143">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="bc563-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="bc563-144">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="bc563-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




