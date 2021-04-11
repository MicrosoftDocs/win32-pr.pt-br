---
description: Habilita o adaptador de rede.
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Método Enable da classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163992"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="f16fa-103">Habilitar o método da \_ classe Win32 adaptador</span><span class="sxs-lookup"><span data-stu-id="f16fa-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="f16fa-104">O método **Enable** habilita o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="f16fa-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f16fa-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="f16fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f16fa-106">Parameters</span></span>

<span data-ttu-id="f16fa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f16fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f16fa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f16fa-108">Return value</span></span>

<span data-ttu-id="f16fa-109">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="f16fa-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="f16fa-110">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="f16fa-110">Any other number indicates an error.</span></span> <span data-ttu-id="f16fa-111">Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f16fa-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="f16fa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f16fa-112">Remarks</span></span>

<span data-ttu-id="f16fa-113">Você pode enfrentar dificuldades ao usar esse método se seu aplicativo não tiver acesso de administrador ao privilidges.</span><span class="sxs-lookup"><span data-stu-id="f16fa-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="f16fa-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f16fa-114">Examples</span></span>

<span data-ttu-id="f16fa-115">O exemplo de script a seguir Visual Basic habilita o primeiro adaptador de rede e mostra o status da propriedade **Nethabilitada** .</span><span class="sxs-lookup"><span data-stu-id="f16fa-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="f16fa-116">Para obter mais informações, consulte [**SWbemObjectSet. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span><span class="sxs-lookup"><span data-stu-id="f16fa-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="f16fa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f16fa-117">Requirements</span></span>



| <span data-ttu-id="f16fa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16fa-118">Requirement</span></span> | <span data-ttu-id="f16fa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f16fa-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f16fa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f16fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f16fa-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f16fa-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f16fa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f16fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f16fa-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f16fa-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f16fa-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f16fa-124">Namespace</span></span><br/>                | <span data-ttu-id="f16fa-125">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f16fa-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f16fa-126">MOF</span><span class="sxs-lookup"><span data-stu-id="f16fa-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f16fa-127"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f16fa-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f16fa-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f16fa-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f16fa-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f16fa-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16fa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f16fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16fa-131">**\_Adaptador Win32**</span><span class="sxs-lookup"><span data-stu-id="f16fa-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="f16fa-132">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="f16fa-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f16fa-133">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="f16fa-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

