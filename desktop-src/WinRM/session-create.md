---
title: Método Session. Create (WSManDisp. h)
description: Cria uma nova instância de um recurso e retorna a referência do ponto de extremidade (EPR) do novo objeto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Criar Gerenciamento Remoto do Windows do método
- Criar Gerenciamento Remoto do Windows do método, objeto Session
- Objeto de sessão Gerenciamento Remoto do Windows, criar método
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455469"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="75402-106">Método Session. Create</span><span class="sxs-lookup"><span data-stu-id="75402-106">Session.Create method</span></span>

<span data-ttu-id="75402-107">Cria uma nova instância de um recurso e retorna a [*referência do ponto de extremidade (EPR)*](windows-remote-management-glossary.md) do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="75402-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75402-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75402-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="75402-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75402-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75402-110">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75402-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75402-111">Identificador do recurso a ser criado.</span><span class="sxs-lookup"><span data-stu-id="75402-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="75402-112">Esse parâmetro pode conter um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="75402-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="75402-113">URI com um ou mais [*seletores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="75402-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="75402-114">Lembre-se de que o [*plug-in WMI*](windows-remote-management-glossary.md) não dá suporte à criação de qualquer recurso que não seja um ouvinte de [protocolo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="75402-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="75402-115">Objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="75402-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="75402-116">Referência de ponto de extremidade [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="75402-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="75402-117">Para obter mais informações sobre a especificação pública para WS-Management protocolo, consulte [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="75402-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="75402-118">*Kit*</span><span class="sxs-lookup"><span data-stu-id="75402-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="75402-119">O XML que contém o conteúdo do recurso.</span><span class="sxs-lookup"><span data-stu-id="75402-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="75402-120">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="75402-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75402-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="75402-121">Reserved.</span></span> <span data-ttu-id="75402-122">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="75402-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75402-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75402-123">Return value</span></span>

<span data-ttu-id="75402-124">O EPR do novo recurso.</span><span class="sxs-lookup"><span data-stu-id="75402-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="75402-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="75402-125">Remarks</span></span>

<span data-ttu-id="75402-126">**Session. Create** é usado somente para criar novas instâncias de um recurso.</span><span class="sxs-lookup"><span data-stu-id="75402-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="75402-127">Use o método [**Session. put**](session-put.md) para atualizar as instâncias existentes de um recurso.</span><span class="sxs-lookup"><span data-stu-id="75402-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="75402-128">Depois de obter o novo URI de recurso, você pode chamar [**Session. Get**](session-get.md) para recuperar o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="75402-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="75402-129">O novo objeto contém todas as propriedades que o provedor de recursos atribui ao criar o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="75402-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="75402-130">Por exemplo, se você criar um novo [*ouvinte*](windows-remote-management-glossary.md) de protocolo WS-Management e recuperar o objeto de ouvinte usando **Session. Get**, também obterá as propriedades **Port**, **Enabled** e **listening** .</span><span class="sxs-lookup"><span data-stu-id="75402-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="75402-131">Lembre-se de que o [*plug-in WMI*](windows-remote-management-glossary.md) não dá suporte à criação de qualquer recurso que não seja um ouvinte de protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="75402-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="75402-132">A sintaxe a seguir é usada para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="75402-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="75402-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75402-133">Examples</span></span>

<span data-ttu-id="75402-134">O exemplo de código VBScript a seguir chama **Session. Create** para criar um ouvinte no computador local.</span><span class="sxs-lookup"><span data-stu-id="75402-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="75402-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75402-135">Requirements</span></span>



| <span data-ttu-id="75402-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="75402-136">Requirement</span></span> | <span data-ttu-id="75402-137">Valor</span><span class="sxs-lookup"><span data-stu-id="75402-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75402-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75402-138">Minimum supported client</span></span><br/> | <span data-ttu-id="75402-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75402-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="75402-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75402-140">Minimum supported server</span></span><br/> | <span data-ttu-id="75402-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75402-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="75402-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75402-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="75402-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75402-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="75402-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="75402-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75402-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75402-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="75402-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75402-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="75402-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75402-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75402-148">DLL</span><span class="sxs-lookup"><span data-stu-id="75402-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75402-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75402-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75402-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="75402-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75402-151">**Session**</span><span class="sxs-lookup"><span data-stu-id="75402-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="75402-152">Protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="75402-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

