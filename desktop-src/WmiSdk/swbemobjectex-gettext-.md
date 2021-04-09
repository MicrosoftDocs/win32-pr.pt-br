---
description: Retorna uma representação XML de um objeto ou instância. O arquivo de texto é formatado no formato XML especificado, conforme mostrado em WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Método de SWbemObjectEx.GetText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011707"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="096c4-104">Método SWbemObjectEx. GetText \_</span><span class="sxs-lookup"><span data-stu-id="096c4-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="096c4-105">O método **gettext \_** do objeto [**SWBEMOBJECTEX**](swbemobjectex.md) retorna uma representação XML de um objeto ou instância.</span><span class="sxs-lookup"><span data-stu-id="096c4-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="096c4-106">O arquivo de texto é formatado no formato XML especificado, conforme mostrado em [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span><span class="sxs-lookup"><span data-stu-id="096c4-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="096c4-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="096c4-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="096c4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="096c4-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="096c4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="096c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="096c4-110">*iTextFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="096c4-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="096c4-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="096c4-111">Required.</span></span> <span data-ttu-id="096c4-112">Um valor de [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) que especifica o formato XML resultante.</span><span class="sxs-lookup"><span data-stu-id="096c4-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="096c4-113">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="096c4-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="096c4-114">Sinalizadores de operação reservados.</span><span class="sxs-lookup"><span data-stu-id="096c4-114">Reserved operation flags.</span></span> <span data-ttu-id="096c4-115">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="096c4-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="096c4-116">*objWbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="096c4-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="096c4-117">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que define o contexto para a operação.</span><span class="sxs-lookup"><span data-stu-id="096c4-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="096c4-118">O padrão é nulo.</span><span class="sxs-lookup"><span data-stu-id="096c4-118">The default is null.</span></span> <span data-ttu-id="096c4-119">Para obter mais informações sobre os pares de nome/valor permitidos, consulte os comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="096c4-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="096c4-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="096c4-120">Return value</span></span>

<span data-ttu-id="096c4-121">Este método não tem valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="096c4-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="096c4-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="096c4-122">Error codes</span></span>

<span data-ttu-id="096c4-123">Após a conclusão do método **gettext \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="096c4-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="096c4-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="096c4-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="096c4-125">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="096c4-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="096c4-126">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="096c4-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="096c4-127">O formato solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="096c4-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="096c4-128">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="096c4-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="096c4-129">Um dos parâmetros para a chamada não está correto.</span><span class="sxs-lookup"><span data-stu-id="096c4-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="096c4-130">**wbemErrCriticalError** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="096c4-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="096c4-131">Ocorreu um erro interno, crítico e inesperado.</span><span class="sxs-lookup"><span data-stu-id="096c4-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="096c4-132">Relate este erro ao Suporte Técnico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="096c4-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="096c4-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="096c4-133">Remarks</span></span>

<span data-ttu-id="096c4-134">Ao construir seu [**SWbemNamedValueSet**](swbemnamedvalueset.md), somente os seguintes pares de nome/valor são permitidos.</span><span class="sxs-lookup"><span data-stu-id="096c4-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="096c4-135">Nome</span><span class="sxs-lookup"><span data-stu-id="096c4-135">Name</span></span></th>
<th><span data-ttu-id="096c4-136">Valor</span><span class="sxs-lookup"><span data-stu-id="096c4-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="096c4-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="096c4-137">LocalOnly</span></span></td>
<td><span data-ttu-id="096c4-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="096c4-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="096c4-139">Se <strong>for true</strong>, somente as propriedades e os métodos definidos localmente estarão presentes no XML resultante.</span><span class="sxs-lookup"><span data-stu-id="096c4-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="096c4-140">O padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="096c4-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="096c4-141">IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="096c4-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="096c4-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="096c4-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="096c4-143">Se <strong>for true</strong>, os qualificadores de classes, instâncias, propriedades e métodos serão incluídos no XML resultante.</span><span class="sxs-lookup"><span data-stu-id="096c4-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="096c4-144">O padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="096c4-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="096c4-145">PathLevel</span><span class="sxs-lookup"><span data-stu-id="096c4-145">PathLevel</span></span></td>
<td><span data-ttu-id="096c4-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="096c4-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="096c4-147">O padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="096c4-147">Default is 0 (zero).</span></span> <span data-ttu-id="096c4-148">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="096c4-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="096c4-149">0: um <CLASS> <INSTANCE> elemento ou é criado dependendo se o objeto é uma classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="096c4-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="096c4-150">1: um <VALUE.NAMEDOBJECT> elemento é gerado.</span><span class="sxs-lookup"><span data-stu-id="096c4-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="096c4-151">2: um <VALUE.OBJECTWITHLOCALPATH> elemento é gerado.</span><span class="sxs-lookup"><span data-stu-id="096c4-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="096c4-152">3: um <VALUE.OBJECTWITHPATH> elemento é gerado.</span><span class="sxs-lookup"><span data-stu-id="096c4-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="096c4-153">ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="096c4-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="096c4-154"><strong>VT-BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="096c4-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="096c4-155">Se <strong>for true</strong>, as propriedades do sistema, como __NAMESPACE, serão excluídas da saída.</span><span class="sxs-lookup"><span data-stu-id="096c4-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="096c4-156">IncludeClassOrigin</span><span class="sxs-lookup"><span data-stu-id="096c4-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="096c4-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="096c4-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="096c4-158">Se <strong>for true</strong>, o atributo de origem da classe será definido nos <PROPERTY> <METHOD> elementos e.</span><span class="sxs-lookup"><span data-stu-id="096c4-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="096c4-159">O padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="096c4-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="096c4-160">Para obter mais informações sobre como criar um [**SWbemNamedValueSet**](swbemnamedvalueset.md), consulte [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).</span><span class="sxs-lookup"><span data-stu-id="096c4-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="096c4-161">Exemplos</span><span class="sxs-lookup"><span data-stu-id="096c4-161">Examples</span></span>

<span data-ttu-id="096c4-162">O script a seguir mostra como obter uma representação XML da definição de classe [**\_ do BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) .</span><span class="sxs-lookup"><span data-stu-id="096c4-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="096c4-163">Ao especificar uma instância específica do **\_ BIOS Win32**, você pode obter os dados desse objeto em XML.</span><span class="sxs-lookup"><span data-stu-id="096c4-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="096c4-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="096c4-164">Requirements</span></span>



| <span data-ttu-id="096c4-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="096c4-165">Requirement</span></span> | <span data-ttu-id="096c4-166">Valor</span><span class="sxs-lookup"><span data-stu-id="096c4-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="096c4-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="096c4-167">Minimum supported client</span></span><br/> | <span data-ttu-id="096c4-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="096c4-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="096c4-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="096c4-169">Minimum supported server</span></span><br/> | <span data-ttu-id="096c4-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="096c4-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="096c4-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="096c4-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="096c4-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="096c4-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="096c4-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="096c4-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="096c4-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="096c4-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="096c4-175">DLL</span><span class="sxs-lookup"><span data-stu-id="096c4-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="096c4-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="096c4-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="096c4-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="096c4-177">CLSID</span></span><br/>                    | <span data-ttu-id="096c4-178">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="096c4-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="096c4-179">IID</span><span class="sxs-lookup"><span data-stu-id="096c4-179">IID</span></span><br/>                      | <span data-ttu-id="096c4-180">ISWbemObjectEx de IID \_</span><span class="sxs-lookup"><span data-stu-id="096c4-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

