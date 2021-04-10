---
title: Método Session. Enumeration (WSManDisp. h)
description: Enumera uma tabela, uma coleção de dados ou um recurso de log.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Enumerate
- Método Enumerate Gerenciamento Remoto do Windows, objeto Session
- Gerenciamento Remoto do Windows de objeto de sessão, método Enumerate
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009139"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="e9402-106">Método Session. Enumeration</span><span class="sxs-lookup"><span data-stu-id="e9402-106">Session.Enumerate method</span></span>

<span data-ttu-id="e9402-107">Enumera uma tabela, uma coleção de dados ou um recurso de log.</span><span class="sxs-lookup"><span data-stu-id="e9402-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="e9402-108">Para criar uma consulta, inclua um parâmetro de *filtro* e um parâmetro de *dialeto* em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="e9402-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="e9402-109">Você também pode usar um objeto [**ResourceLocator**](resourcelocator.md) para criar consultas.</span><span class="sxs-lookup"><span data-stu-id="e9402-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="e9402-110">Para obter mais informações, consulte [enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="e9402-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9402-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9402-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e9402-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9402-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9402-113">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9402-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9402-114">O identificador do recurso a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e9402-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="e9402-115">Esse parâmetro pode conter um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="e9402-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="e9402-116">O URI do recurso.</span><span class="sxs-lookup"><span data-stu-id="e9402-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="e9402-117">Um objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e9402-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="e9402-118">Uma referência de ponto de extremidade do [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="e9402-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="e9402-119">Para obter mais informações sobre a especificação pública para [protocolo WS-Management](ws-management-protocol.md), consulte a [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="e9402-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="e9402-120">*Filtrar* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9402-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9402-121">Um filtro que define quais itens no recurso são retornados pela enumeração.</span><span class="sxs-lookup"><span data-stu-id="e9402-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="e9402-122">Quando o recurso é enumerado, somente os itens que correspondem aos critérios de filtro são retornados.</span><span class="sxs-lookup"><span data-stu-id="e9402-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="e9402-123">A inclusão de um parâmetro de *filtro* e um parâmetro de *dialeto* em uma enumeração converte a enumeração em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="e9402-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="e9402-124">Para obter um exemplo, consulte [consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="e9402-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="e9402-125">Se você tiver um objeto [**ResourceLocator**](resourcelocator.md) para o parâmetro *ResourceURI* , esse parâmetro não deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="e9402-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="e9402-126">*dialeto* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9402-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9402-127">O idioma usado pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="e9402-127">The language used by the filter.</span></span> <span data-ttu-id="e9402-128">O [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), um subconjunto de SQL usado pelo WMI, é o único idioma com suporte.</span><span class="sxs-lookup"><span data-stu-id="e9402-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="e9402-129">Se você tiver um objeto [**ResourceLocator**](resourcelocator.md) para o parâmetro *ResourceURI* , esse parâmetro não deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="e9402-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="e9402-130">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9402-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9402-131">Um parâmetro que deve conter um sinalizador na enumeração **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="e9402-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="e9402-132">Para obter mais informações, consulte [constantes de enumeração](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e9402-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9402-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9402-133">Return value</span></span>

<span data-ttu-id="e9402-134">Um objeto [**enumerador**](enumerator.md) que contém os resultados da enumeração.</span><span class="sxs-lookup"><span data-stu-id="e9402-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9402-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9402-135">Remarks</span></span>

<span data-ttu-id="e9402-136">Para obter mais informações sobre como limitar chamadas de rede durante uma enumeração, consulte a propriedade [**BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="e9402-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="e9402-137">Lembre-se de que, se os sinalizadores incluírem as [**constantes de enumeração**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , gerenciamento remoto do Windows serviço retornará o erro de código de erro o **modo de polimorfismo do \_ WSMan \_ \_ \_ sem suporte**.</span><span class="sxs-lookup"><span data-stu-id="e9402-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="e9402-138">Se um filtro for especificado, ele deverá ser um documento válido em relação ao esquema do recurso.</span><span class="sxs-lookup"><span data-stu-id="e9402-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="e9402-139">O parâmetro dialeto é opcional.</span><span class="sxs-lookup"><span data-stu-id="e9402-139">The dialect parameter is optional.</span></span> <span data-ttu-id="e9402-140">No entanto, se a cadeia de caracteres de filtro começar com <, mas não for um fragmento XML, inclua o parâmetro *dialeto* ou defina o sinalizador **WSManFlagNonXmlText** no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="e9402-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="e9402-141">Para obter mais informações, consulte [**constantes de enumeração**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e9402-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="e9402-142">O método C++ correspondente é [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="e9402-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="e9402-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9402-143">Examples</span></span>

<span data-ttu-id="e9402-144">O exemplo de código VBScript a seguir enumera as instâncias do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em um computador remoto especificado pelo servername.domain.com (nome de domínio totalmente qualificado).</span><span class="sxs-lookup"><span data-stu-id="e9402-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="e9402-145">Lembre-se de que a liberação do objeto de enumeração limpa as solicitações de enumeração pendentes.</span><span class="sxs-lookup"><span data-stu-id="e9402-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="e9402-146">A sub-rotina DisplayOutput usa o arquivo de transformação XML da ferramenta de linha de comando do WinRM (WsmTxt. Xsl) para gerar os dados em um formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="e9402-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e9402-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9402-147">Requirements</span></span>



| <span data-ttu-id="e9402-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9402-148">Requirement</span></span> | <span data-ttu-id="e9402-149">Valor</span><span class="sxs-lookup"><span data-stu-id="e9402-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9402-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9402-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e9402-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9402-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e9402-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9402-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e9402-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9402-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e9402-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9402-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9402-155"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9402-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9402-156">INSERI</span><span class="sxs-lookup"><span data-stu-id="e9402-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9402-157"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9402-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e9402-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9402-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9402-159"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9402-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9402-160">DLL</span><span class="sxs-lookup"><span data-stu-id="e9402-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9402-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9402-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9402-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9402-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9402-163">**Session**</span><span class="sxs-lookup"><span data-stu-id="e9402-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="e9402-164">Consultando instâncias específicas de um recurso</span><span class="sxs-lookup"><span data-stu-id="e9402-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="e9402-165">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="e9402-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="e9402-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="e9402-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

