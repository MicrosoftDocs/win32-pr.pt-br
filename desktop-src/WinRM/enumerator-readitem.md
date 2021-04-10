---
title: Método Enumerator. ReadItem (WSManDisp. h)
description: Recupera um item do recurso e retorna uma representação XML do item.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método ReadItem
- Método ReadItem Gerenciamento Remoto do Windows, objeto Enumerator
- Objeto Enumerator Gerenciamento Remoto do Windows, método ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009140"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="7eae9-106">Método Enumerator. ReadItem</span><span class="sxs-lookup"><span data-stu-id="7eae9-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="7eae9-107">Recupera um item do recurso e retorna uma representação XML do item.</span><span class="sxs-lookup"><span data-stu-id="7eae9-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eae9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eae9-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="7eae9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7eae9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eae9-110">*Kit*</span><span class="sxs-lookup"><span data-stu-id="7eae9-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="7eae9-111">O URI do item.</span><span class="sxs-lookup"><span data-stu-id="7eae9-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eae9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7eae9-112">Return value</span></span>

<span data-ttu-id="7eae9-113">A representação XML do item.</span><span class="sxs-lookup"><span data-stu-id="7eae9-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eae9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eae9-114">Remarks</span></span>

<span data-ttu-id="7eae9-115">Para limitar o número de itens lidos, defina a propriedade [**Session.BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="7eae9-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="7eae9-116">Observe que a liberação do objeto de enumeração limpa todas as solicitações de enumeração pendentes.</span><span class="sxs-lookup"><span data-stu-id="7eae9-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="7eae9-117">O método [**Session. Enumerate**](session-enumerate.md) não obtém uma coleção da mesma maneira que uma [consulta WMI](/windows/desktop/WmiSdk/querying-wmi), como `SELECT * from Win32_LogicalDisk` , retorna uma coleção em um [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span><span class="sxs-lookup"><span data-stu-id="7eae9-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="7eae9-118">Para ler um arquivo como um fluxo de texto, crie o objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script e chame o método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para ler cada linha do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7eae9-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="7eae9-119">De forma semelhante, você chama o método **Session. enumerar** para obter um objeto [**Enumerator**](enumerator.md) e, em seguida, chamar o método **Enumerator. ReadItem** .</span><span class="sxs-lookup"><span data-stu-id="7eae9-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="7eae9-120">Como na leitura do arquivo de texto, você pode verificar a propriedade [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) para verificar se você atingiu o final dos itens de dados.</span><span class="sxs-lookup"><span data-stu-id="7eae9-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="7eae9-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7eae9-121">Examples</span></span>

<span data-ttu-id="7eae9-122">O exemplo de VBScript a seguir chama o método [**Session. enumerar**](session-enumerate.md) para obter uma lista de trabalhos agendados.</span><span class="sxs-lookup"><span data-stu-id="7eae9-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="7eae9-123">A sub-rotina DisplayOutput usa o arquivo de transformação XML da ferramenta de linha de comando do WinRM (WsmTxt. Xsl) para gerar os dados em um formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="7eae9-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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



## <a name="requirements"></a><span data-ttu-id="7eae9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eae9-124">Requirements</span></span>



| <span data-ttu-id="7eae9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eae9-125">Requirement</span></span> | <span data-ttu-id="7eae9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7eae9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eae9-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eae9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7eae9-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eae9-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7eae9-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eae9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7eae9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eae9-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7eae9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7eae9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eae9-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7eae9-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7eae9-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="7eae9-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7eae9-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7eae9-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7eae9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7eae9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7eae9-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7eae9-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7eae9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7eae9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eae9-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eae9-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7eae9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eae9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eae9-140">**Enumerador**</span><span class="sxs-lookup"><span data-stu-id="7eae9-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="7eae9-141">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="7eae9-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

