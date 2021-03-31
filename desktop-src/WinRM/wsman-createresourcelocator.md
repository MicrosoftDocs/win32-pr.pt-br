---
title: Método WSMan. CreateResourceLocator (WSManDisp. h)
description: Cria um objeto ResourceLocator que pode ser usado em vez de especificar um URI de recurso em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método CreateResourceLocator
- Método CreateResourceLocator Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918362"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="76d77-106">Método WSMan. CreateResourceLocator</span><span class="sxs-lookup"><span data-stu-id="76d77-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="76d77-107">Cria um objeto [**ResourceLocator**](resourcelocator.md) que pode ser usado em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="76d77-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76d77-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76d77-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="76d77-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76d77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d77-110">*URI* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="76d77-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76d77-111">O URI de recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="76d77-111">The resource URI for the resource.</span></span> <span data-ttu-id="76d77-112">Para obter mais informações sobre cadeias de caracteres de URI, consulte [URIs de recurso](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="76d77-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d77-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76d77-113">Return value</span></span>

<span data-ttu-id="76d77-114">Um objeto [**ResourceLocator**](resourcelocator.md) que pode ser usado para executar operações WinRM locais ou remotas.</span><span class="sxs-lookup"><span data-stu-id="76d77-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d77-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="76d77-115">Remarks</span></span>

<span data-ttu-id="76d77-116">Se a propriedade **FragmentDialect** não for especificada no objeto [**ResourceLocator**](resourcelocator.md) , o padrão será a especificação XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="76d77-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="76d77-117">Para obter mais informações, confira [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="76d77-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="76d77-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76d77-118">Examples</span></span>

<span data-ttu-id="76d77-119">O exemplo de código VBScript a seguir cria um objeto [**ResourceLocator**](resourcelocator.md) e Obtém o valor da propriedade de **Descrição** do adaptador de rede da instância do [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) com um índice de "1".</span><span class="sxs-lookup"><span data-stu-id="76d77-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="76d77-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76d77-120">Requirements</span></span>



| <span data-ttu-id="76d77-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d77-121">Requirement</span></span> | <span data-ttu-id="76d77-122">Valor</span><span class="sxs-lookup"><span data-stu-id="76d77-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d77-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d77-123">Minimum supported client</span></span><br/> | <span data-ttu-id="76d77-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76d77-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="76d77-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d77-125">Minimum supported server</span></span><br/> | <span data-ttu-id="76d77-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76d77-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="76d77-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76d77-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d77-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d77-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="76d77-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="76d77-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76d77-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76d77-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="76d77-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76d77-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="76d77-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76d77-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76d77-133">DLL</span><span class="sxs-lookup"><span data-stu-id="76d77-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76d77-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76d77-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76d77-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="76d77-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d77-136">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="76d77-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="76d77-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="76d77-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="76d77-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="76d77-138">**Session**</span></span>](session.md)
</dt> </dl>

 

