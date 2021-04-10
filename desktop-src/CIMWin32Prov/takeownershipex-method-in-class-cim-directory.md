---
description: Obtém a propriedade do arquivo de entrada de diretório lógico especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip e é herdado do \_ LogicalFile. CIM.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088939"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="4b25e-104">Método TakeOwnerShipEx da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="4b25e-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="4b25e-105">O método **TakeOwnerShipEx** Obtém a propriedade do arquivo de entrada de diretório lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="4b25e-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="4b25e-106">Esse método é uma versão estendida do método [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) e é herdado [**do \_ LogicalFile. CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4b25e-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="4b25e-107">Se o arquivo lógico for um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="4b25e-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b25e-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4b25e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b25e-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b25e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b25e-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4b25e-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4b25e-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4b25e-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b25e-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b25e-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4b25e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b25e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b25e-114">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4b25e-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25e-115">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="4b25e-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4b25e-116">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="4b25e-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4b25e-117">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b25e-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25e-118">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="4b25e-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="4b25e-119">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="4b25e-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4b25e-120">Se esse parâmetro for nulo, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="4b25e-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="4b25e-121">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b25e-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25e-122">Se **for true**, o método será aplicado recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância do [**\_ diretório CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="4b25e-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="4b25e-123">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="4b25e-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b25e-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b25e-124">Return value</span></span>

<span data-ttu-id="4b25e-125">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="4b25e-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-126">0</span><span class="sxs-lookup"><span data-stu-id="4b25e-126">0</span></span>

<span data-ttu-id="4b25e-127">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="4b25e-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-128">2</span><span class="sxs-lookup"><span data-stu-id="4b25e-128">2</span></span>

<span data-ttu-id="4b25e-129">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="4b25e-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-130">8</span><span class="sxs-lookup"><span data-stu-id="4b25e-130">8</span></span>

<span data-ttu-id="4b25e-131">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="4b25e-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-132">9</span><span class="sxs-lookup"><span data-stu-id="4b25e-132">9</span></span>

<span data-ttu-id="4b25e-133">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="4b25e-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-134">10</span><span class="sxs-lookup"><span data-stu-id="4b25e-134">10</span></span>

<span data-ttu-id="4b25e-135">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="4b25e-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-136">11</span><span class="sxs-lookup"><span data-stu-id="4b25e-136">11</span></span>

<span data-ttu-id="4b25e-137">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="4b25e-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-138">12</span><span class="sxs-lookup"><span data-stu-id="4b25e-138">12</span></span>

<span data-ttu-id="4b25e-139">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="4b25e-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-140">13</span><span class="sxs-lookup"><span data-stu-id="4b25e-140">13</span></span>

<span data-ttu-id="4b25e-141">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="4b25e-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-142">14</span><span class="sxs-lookup"><span data-stu-id="4b25e-142">14</span></span>

<span data-ttu-id="4b25e-143">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="4b25e-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-144">15</span><span class="sxs-lookup"><span data-stu-id="4b25e-144">15</span></span>

<span data-ttu-id="4b25e-145">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="4b25e-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-146">16</span><span class="sxs-lookup"><span data-stu-id="4b25e-146">16</span></span>

<span data-ttu-id="4b25e-147">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="4b25e-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-148">17</span><span class="sxs-lookup"><span data-stu-id="4b25e-148">17</span></span>

<span data-ttu-id="4b25e-149">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="4b25e-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4b25e-150">21</span><span class="sxs-lookup"><span data-stu-id="4b25e-150">21</span></span>

<span data-ttu-id="4b25e-151">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="4b25e-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b25e-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b25e-152">Remarks</span></span>

<span data-ttu-id="4b25e-153">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="4b25e-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4b25e-154">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="4b25e-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4b25e-155">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b25e-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b25e-156">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4b25e-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="4b25e-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b25e-157">Examples</span></span>

<span data-ttu-id="4b25e-158">O código de script Visual Basic a seguir chama o método **TakeOwnerShipEx** para apropriar-se da pasta C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="4b25e-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="4b25e-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b25e-159">Requirements</span></span>



| <span data-ttu-id="4b25e-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b25e-160">Requirement</span></span> | <span data-ttu-id="4b25e-161">Valor</span><span class="sxs-lookup"><span data-stu-id="4b25e-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b25e-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b25e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="4b25e-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b25e-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b25e-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b25e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="4b25e-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b25e-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b25e-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b25e-166">Namespace</span></span><br/>                | <span data-ttu-id="4b25e-167">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4b25e-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b25e-168">MOF</span><span class="sxs-lookup"><span data-stu-id="4b25e-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b25e-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b25e-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b25e-170">DLL</span><span class="sxs-lookup"><span data-stu-id="4b25e-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b25e-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b25e-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b25e-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b25e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b25e-173">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="4b25e-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="4b25e-174">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="4b25e-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

