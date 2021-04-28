---
description: Método GetAccessMask da classe Win32_Share – retorna um bitmap UInt32 com os direitos de acesso ao compartilhamento mantido pelo usuário ou grupo em cujo nome a instância é retornada.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Método GetAccessMask da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fcd6396f6421060a67108e7c428c99bcd7ca9651
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097014"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="41175-103">Método GetAccessMask da classe de \_ compartilhamento do Win32</span><span class="sxs-lookup"><span data-stu-id="41175-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="41175-104">O método **GetAccessMask** retorna um bitmap UInt32 com os direitos de acesso ao compartilhamento mantido pelo usuário ou grupo em cujo nome a instância é retornada.</span><span class="sxs-lookup"><span data-stu-id="41175-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="41175-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="41175-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41175-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="41175-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41175-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41175-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="41175-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41175-108">Parameters</span></span>

<span data-ttu-id="41175-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="41175-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41175-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="41175-110">Return value</span></span>

<span data-ttu-id="41175-111">Direitos de acesso ao compartilhamento mantido pelo usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="41175-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="41175-112">**\_diretório de lista de arquivos \_**</span><span class="sxs-lookup"><span data-stu-id="41175-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="41175-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="41175-113">1 (0x1)</span></span>

<span data-ttu-id="41175-114">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="41175-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="41175-115">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="41175-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="41175-116">**ARQUIVO- \_ Adicionar \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="41175-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="41175-117">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="41175-117">2 (0x2)</span></span>

<span data-ttu-id="41175-118">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="41175-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="41175-119">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="41175-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="41175-120">**ARQUIVO \_ Adicionar \_ subdiretório**</span><span class="sxs-lookup"><span data-stu-id="41175-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="41175-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="41175-121">4 (0x4)</span></span>

<span data-ttu-id="41175-122">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="41175-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="41175-123">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="41175-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="41175-124">**ARQUIVO de \_ leitura \_ ea**</span><span class="sxs-lookup"><span data-stu-id="41175-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="41175-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="41175-125">8 (0x8)</span></span>

<span data-ttu-id="41175-126">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="41175-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="41175-127">**\_ea de gravação de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="41175-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="41175-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="41175-128">16 (0x10)</span></span>

<span data-ttu-id="41175-129">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="41175-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="41175-130">**\_atravessamento de arquivo**</span><span class="sxs-lookup"><span data-stu-id="41175-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="41175-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="41175-131">32 (0x20)</span></span>

<span data-ttu-id="41175-132">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="41175-132">Grants the right to execute a file.</span></span> <span data-ttu-id="41175-133">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="41175-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="41175-134">**\_excluir arquivo \_ filho**</span><span class="sxs-lookup"><span data-stu-id="41175-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="41175-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="41175-135">64 (0x40)</span></span>

<span data-ttu-id="41175-136">Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="41175-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="41175-137">**\_atributos de leitura de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="41175-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="41175-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="41175-138">128 (0x80)</span></span>

<span data-ttu-id="41175-139">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="41175-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="41175-140">**\_atributos de gravação de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="41175-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="41175-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="41175-141">256 (0x100)</span></span>

<span data-ttu-id="41175-142">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="41175-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="41175-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="41175-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="41175-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="41175-144">65536 (0x10000)</span></span>

<span data-ttu-id="41175-145">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="41175-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="41175-146">**controle de leitura \_**</span><span class="sxs-lookup"><span data-stu-id="41175-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="41175-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="41175-147">131072 (0x20000)</span></span>

<span data-ttu-id="41175-148">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="41175-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="41175-149">**GRAVAR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="41175-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="41175-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="41175-150">262144 (0x40000)</span></span>

<span data-ttu-id="41175-151">Concede acesso de gravação à DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="41175-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="41175-152">**proprietário da gravação \_**</span><span class="sxs-lookup"><span data-stu-id="41175-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="41175-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="41175-153">524288 (0x80000)</span></span>

<span data-ttu-id="41175-154">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="41175-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="41175-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="41175-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="41175-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="41175-156">1048576 (0x100000)</span></span>

<span data-ttu-id="41175-157">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="41175-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41175-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="41175-158">Remarks</span></span>

<span data-ttu-id="41175-159">O método **GetAccessMask** é um método de objeto e é usado em uma ocorrência dessa classe.</span><span class="sxs-lookup"><span data-stu-id="41175-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="41175-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41175-160">Examples</span></span>

<span data-ttu-id="41175-161">O exemplo de código VBScript a seguir cria uma pasta de compartilhamento e Obtém o valor da máscara de acesso no descritor de segurança que protege a pasta de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="41175-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="41175-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41175-162">Requirements</span></span>



| <span data-ttu-id="41175-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="41175-163">Requirement</span></span> | <span data-ttu-id="41175-164">Valor</span><span class="sxs-lookup"><span data-stu-id="41175-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41175-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41175-165">Minimum supported client</span></span><br/> | <span data-ttu-id="41175-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41175-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41175-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41175-167">Minimum supported server</span></span><br/> | <span data-ttu-id="41175-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41175-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41175-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="41175-169">Namespace</span></span><br/>                | <span data-ttu-id="41175-170">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="41175-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41175-171">MOF</span><span class="sxs-lookup"><span data-stu-id="41175-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41175-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41175-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41175-173">DLL</span><span class="sxs-lookup"><span data-stu-id="41175-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41175-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41175-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41175-175">Consulte também</span><span class="sxs-lookup"><span data-stu-id="41175-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41175-176">**Compartilhamento do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="41175-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

