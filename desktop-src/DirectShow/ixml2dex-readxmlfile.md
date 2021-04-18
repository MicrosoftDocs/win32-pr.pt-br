---
description: O método ReadXMLfile carrega um arquivo de projeto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'Método IXml2Dex:: ReadXMLfile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760083"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="9e7fa-103">Método IXml2Dex:: ReadXMLfile</span><span class="sxs-lookup"><span data-stu-id="9e7fa-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="9e7fa-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-104">\[Deprecated.</span></span> <span data-ttu-id="9e7fa-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e7fa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e7fa-106">O `ReadXMLFile` método carrega um arquivo de projeto XML.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="9e7fa-107">Esse método cria instâncias de todos os objetos expressos no arquivo XML e os insere na linha do tempo, bem como aplica os atributos fornecidos para a linha do tempo, como a taxa de quadros ou o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7fa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e7fa-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="9e7fa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e7fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7fa-110">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="9e7fa-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="9e7fa-111">Ponteiro para a interface **IUnknown** de um objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="9e7fa-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="9e7fa-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="9e7fa-113">Cadeia de caracteres que especifica o nome do arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7fa-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e7fa-114">Return value</span></span>

<span data-ttu-id="9e7fa-115">Retorna um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-115">Returns an HRESULT value.</span></span> <span data-ttu-id="9e7fa-116">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-116">Possible values include the following.</span></span>



| <span data-ttu-id="9e7fa-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9e7fa-117">Return code</span></span>                                                                                                  | <span data-ttu-id="9e7fa-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e7fa-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="9e7fa-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e7fa-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="9e7fa-120">Sucesso</span><span class="sxs-lookup"><span data-stu-id="9e7fa-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="9e7fa-121"><dt>**VFW \_ E \_ \_ formato de arquivo inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e7fa-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="9e7fa-122">Formato de arquivo inválido</span><span class="sxs-lookup"><span data-stu-id="9e7fa-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e7fa-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e7fa-123">Remarks</span></span>

<span data-ttu-id="9e7fa-124">Esse método não limpa os objetos existentes da linha do tempo antes de inserir os novos objetos definidos no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="9e7fa-125">Se você precisar atualizar uma linha do tempo existente, chame [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) primeiro.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="9e7fa-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e7fa-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e7fa-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e7fa-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9e7fa-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e7fa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e7fa-129">Requirements</span></span>



| <span data-ttu-id="9e7fa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e7fa-130">Requirement</span></span> | <span data-ttu-id="9e7fa-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9e7fa-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7fa-132">Versão</span><span class="sxs-lookup"><span data-stu-id="9e7fa-132">Version</span></span><br/> | <span data-ttu-id="9e7fa-133">Internet Explorer 4,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9e7fa-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="9e7fa-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e7fa-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9e7fa-135"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7fa-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e7fa-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e7fa-136">Library</span></span><br/> | <dl> <span data-ttu-id="9e7fa-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e7fa-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7fa-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e7fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7fa-139">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="9e7fa-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="9e7fa-140">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="9e7fa-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




