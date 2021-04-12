---
description: Exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor, desconectando as conexões com o recurso compartilhado.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Método Delete da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089257"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="28766-103">Método Delete da classe de \_ compartilhamento Win32</span><span class="sxs-lookup"><span data-stu-id="28766-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="28766-104">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor, desconectando as conexões com o recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="28766-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="28766-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="28766-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="28766-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="28766-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="28766-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28766-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="28766-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28766-108">Parameters</span></span>

<span data-ttu-id="28766-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="28766-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28766-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28766-110">Return value</span></span>

<span data-ttu-id="28766-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="28766-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="28766-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="28766-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="28766-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="28766-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="28766-114">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="28766-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28766-115">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="28766-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="28766-116">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="28766-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="28766-117">**Nome inválido** (9)</span><span class="sxs-lookup"><span data-stu-id="28766-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="28766-118">**Nível inválido** (10)</span><span class="sxs-lookup"><span data-stu-id="28766-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="28766-119">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="28766-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="28766-120">**Compartilhamento duplicado** (22)</span><span class="sxs-lookup"><span data-stu-id="28766-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="28766-121">**Caminho Redirecionado** (23)</span><span class="sxs-lookup"><span data-stu-id="28766-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="28766-122">**Dispositivo ou diretório desconhecido** (24)</span><span class="sxs-lookup"><span data-stu-id="28766-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="28766-123">**Nome de rede não encontrado** (25)</span><span class="sxs-lookup"><span data-stu-id="28766-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="28766-124">**Outro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="28766-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="28766-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="28766-125">Remarks</span></span>

<span data-ttu-id="28766-126">O método **delete** é um método Object e é usado em uma instância de uma classe.</span><span class="sxs-lookup"><span data-stu-id="28766-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="28766-127">Somente os membros do grupo local Administradores ou operadores de conta ou aqueles com a associação de grupo de operador de servidor, impressão ou comunicação podem executar o método com êxito.</span><span class="sxs-lookup"><span data-stu-id="28766-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="28766-128">O operador Print só pode excluir filas de impressora.</span><span class="sxs-lookup"><span data-stu-id="28766-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="28766-129">O operador de comunicação pode excluir somente filas de dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="28766-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="28766-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="28766-130">Examples</span></span>

<span data-ttu-id="28766-131">O exemplo de código VBScript a seguir exclui o compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="28766-131">The following VBScript code sample deletes the specified share.</span></span>


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



<span data-ttu-id="28766-132">O exemplo de código do PowerShell a seguir exclui os compartilhamentos em branco.</span><span class="sxs-lookup"><span data-stu-id="28766-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="28766-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28766-133">Requirements</span></span>



| <span data-ttu-id="28766-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="28766-134">Requirement</span></span> | <span data-ttu-id="28766-135">Valor</span><span class="sxs-lookup"><span data-stu-id="28766-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28766-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28766-136">Minimum supported client</span></span><br/> | <span data-ttu-id="28766-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28766-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28766-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28766-138">Minimum supported server</span></span><br/> | <span data-ttu-id="28766-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28766-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28766-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="28766-140">Namespace</span></span><br/>                | <span data-ttu-id="28766-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="28766-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28766-142">MOF</span><span class="sxs-lookup"><span data-stu-id="28766-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28766-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28766-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28766-144">DLL</span><span class="sxs-lookup"><span data-stu-id="28766-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28766-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28766-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28766-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="28766-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="28766-147">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28766-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28766-148">**Compartilhamento do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="28766-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

