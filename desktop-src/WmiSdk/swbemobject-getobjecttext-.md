---
description: O \_ método GetObjectText do objeto SWbemObject retorna uma renderização textual do objeto.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Método de SWbemObject.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749469"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="8a36a-103">Método SWbemObject. GetObjectText \_</span><span class="sxs-lookup"><span data-stu-id="8a36a-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="8a36a-104">O **método \_ GetObjectText** do objeto [**SWbemObject**](swbemobject.md) retorna uma renderização textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a36a-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="8a36a-105">Esse objeto pode ser usado para exibir o conteúdo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8a36a-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="8a36a-106">Atualmente, há suporte apenas para a sintaxe do MOF como um formato de saída.</span><span class="sxs-lookup"><span data-stu-id="8a36a-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="8a36a-107">Observe que o texto MOF retornado não contém todas as informações sobre o objeto; o texto MOF contém apenas informações suficientes para que o compilador MOF possa recriar o objeto original.</span><span class="sxs-lookup"><span data-stu-id="8a36a-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="8a36a-108">Por exemplo, não há informações sobre os qualificadores propagados ou as propriedades da classe pai.</span><span class="sxs-lookup"><span data-stu-id="8a36a-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="8a36a-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8a36a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a36a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a36a-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8a36a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a36a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a36a-112">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a36a-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a36a-113">Reservado e deve ser 0 (zero) se especificado.</span><span class="sxs-lookup"><span data-stu-id="8a36a-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a36a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a36a-114">Return value</span></span>

<span data-ttu-id="8a36a-115">Se for bem-sucedido, esse método retornará uma cadeia de caracteres que contém o texto de saída.</span><span class="sxs-lookup"><span data-stu-id="8a36a-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a36a-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8a36a-116">Error codes</span></span>

<span data-ttu-id="8a36a-117">Após a conclusão do método **GetObjectText \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a36a-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8a36a-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8a36a-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8a36a-119">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8a36a-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8a36a-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8a36a-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8a36a-121">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="8a36a-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="8a36a-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8a36a-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8a36a-123">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="8a36a-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8a36a-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a36a-124">Examples</span></span>

<span data-ttu-id="8a36a-125">O código a seguir, extraído da [lista a definição de uma classe WMI no formato MOF](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) de exemplo de código VBScript na galeria do TechNet, recupera e exibe a representação textual de uma definição de classe WMI na sintaxe MOF (formato MOF).</span><span class="sxs-lookup"><span data-stu-id="8a36a-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="8a36a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a36a-126">Requirements</span></span>



| <span data-ttu-id="8a36a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a36a-127">Requirement</span></span> | <span data-ttu-id="8a36a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8a36a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a36a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a36a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a36a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a36a-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a36a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a36a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a36a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a36a-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a36a-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a36a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a36a-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a36a-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a36a-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a36a-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a36a-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a36a-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a36a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8a36a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a36a-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a36a-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a36a-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a36a-139">CLSID</span></span><br/>                    | <span data-ttu-id="8a36a-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="8a36a-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8a36a-141">IID</span><span class="sxs-lookup"><span data-stu-id="8a36a-141">IID</span></span><br/>                      | <span data-ttu-id="8a36a-142">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="8a36a-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




