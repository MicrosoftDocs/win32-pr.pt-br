---
title: Propriedade Enumerator. AtEndOfStream (WSManDisp. h)
description: Obtém um valor booliano que indica se há mais itens na coleção.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade AtEndOfStream
- Gerenciamento Remoto do Windows da propriedade AtEndOfStream, objeto Enumerator
- Objeto Enumerator Gerenciamento Remoto do Windows, Propriedade AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085356"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="9c4fd-106">Propriedade Enumerator. AtEndOfStream</span><span class="sxs-lookup"><span data-stu-id="9c4fd-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="9c4fd-107">Obtém um valor booliano que indica se há mais itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="9c4fd-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4fd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c4fd-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="9c4fd-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9c4fd-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="9c4fd-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span><span class="sxs-lookup"><span data-stu-id="9c4fd-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="9c4fd-112">Não há mais itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="9c4fd-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**For**</span><span class="sxs-lookup"><span data-stu-id="9c4fd-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="9c4fd-114">Há mais itens disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c4fd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c4fd-115">Remarks</span></span>

<span data-ttu-id="9c4fd-116">Se você liberar o objeto [**enumerador**](enumerator.md) depois de ter obtido todos os dados necessários, todas as solicitações de enumeração pendentes serão removidas.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="9c4fd-117">Para obter mais informações, consulte [enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="9c4fd-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9c4fd-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c4fd-118">Examples</span></span>

<span data-ttu-id="9c4fd-119">O exemplo de VBScript a seguir enumera as instâncias do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="9c4fd-120">Observe que a liberação do objeto de enumeração limpa todas as solicitações de enumeração pendentes.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="9c4fd-121">A sub-rotina DisplayOutput formata a saída de dados da mesma maneira que a ferramenta WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="9c4fd-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

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



## <a name="requirements"></a><span data-ttu-id="9c4fd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c4fd-122">Requirements</span></span>



| <span data-ttu-id="9c4fd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c4fd-123">Requirement</span></span> | <span data-ttu-id="9c4fd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9c4fd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c4fd-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c4fd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9c4fd-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c4fd-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9c4fd-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c4fd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9c4fd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c4fd-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9c4fd-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c4fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c4fd-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c4fd-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c4fd-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="9c4fd-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c4fd-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c4fd-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9c4fd-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c4fd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c4fd-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c4fd-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c4fd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9c4fd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c4fd-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c4fd-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c4fd-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c4fd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c4fd-138">**Enumerador**</span><span class="sxs-lookup"><span data-stu-id="9c4fd-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="9c4fd-139">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="9c4fd-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





