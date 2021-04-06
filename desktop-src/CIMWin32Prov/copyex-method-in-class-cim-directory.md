---
description: O método CopyEx copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro FileName. Esse método é uma versão estendida do método Copy e é herdado de CIM \_ LogicalFile.
ms.assetid: e207cc80-055e-41bc-ab80-dc50131b544d
ms.tgt_platform: multiple
title: Método CopyEx da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d7502c46c616d9b8e1fffeebf5aefcd022dd4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920217"
---
# <a name="copyex-method-of-the-cim_directory-class"></a><span data-ttu-id="26152-104">Método CopyEx da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="26152-104">CopyEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="26152-105">O método **CopyEx** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="26152-105">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="26152-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-cim-directory.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="26152-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26152-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="26152-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26152-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="26152-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26152-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="26152-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="26152-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="26152-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="26152-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26152-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string REF FileName,
  [out] string     StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="26152-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26152-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26152-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26152-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26152-114">Nome totalmente qualificado da cópia do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="26152-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="26152-115">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="26152-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="26152-116">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="26152-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26152-117">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="26152-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="26152-118">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="26152-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="26152-119">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26152-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26152-120">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="26152-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="26152-121">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="26152-121">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="26152-122">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="26152-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="26152-123">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26152-123">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26152-124">Se for TRUE, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ diretório CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="26152-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="26152-125">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="26152-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26152-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26152-126">Return value</span></span>

<span data-ttu-id="26152-127">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="26152-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="26152-128">0</span><span class="sxs-lookup"><span data-stu-id="26152-128">0</span></span>

<span data-ttu-id="26152-129">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="26152-129">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-130">2</span><span class="sxs-lookup"><span data-stu-id="26152-130">2</span></span>

<span data-ttu-id="26152-131">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="26152-131">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-132">8</span><span class="sxs-lookup"><span data-stu-id="26152-132">8</span></span>

<span data-ttu-id="26152-133">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="26152-133">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-134">9</span><span class="sxs-lookup"><span data-stu-id="26152-134">9</span></span>

<span data-ttu-id="26152-135">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="26152-135">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-136">10</span><span class="sxs-lookup"><span data-stu-id="26152-136">10</span></span>

<span data-ttu-id="26152-137">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="26152-137">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-138">11</span><span class="sxs-lookup"><span data-stu-id="26152-138">11</span></span>

<span data-ttu-id="26152-139">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="26152-139">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-140">12</span><span class="sxs-lookup"><span data-stu-id="26152-140">12</span></span>

<span data-ttu-id="26152-141">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="26152-141">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-142">13</span><span class="sxs-lookup"><span data-stu-id="26152-142">13</span></span>

<span data-ttu-id="26152-143">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="26152-143">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-144">14</span><span class="sxs-lookup"><span data-stu-id="26152-144">14</span></span>

<span data-ttu-id="26152-145">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="26152-145">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-146">15</span><span class="sxs-lookup"><span data-stu-id="26152-146">15</span></span>

<span data-ttu-id="26152-147">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="26152-147">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-148">16</span><span class="sxs-lookup"><span data-stu-id="26152-148">16</span></span>

<span data-ttu-id="26152-149">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="26152-149">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-150">17</span><span class="sxs-lookup"><span data-stu-id="26152-150">17</span></span>

<span data-ttu-id="26152-151">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="26152-151">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="26152-152">21</span><span class="sxs-lookup"><span data-stu-id="26152-152">21</span></span>

<span data-ttu-id="26152-153">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="26152-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26152-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="26152-154">Remarks</span></span>

<span data-ttu-id="26152-155">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="26152-155">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="26152-156">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="26152-156">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="26152-157">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="26152-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26152-158">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="26152-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26152-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26152-159">Requirements</span></span>



| <span data-ttu-id="26152-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="26152-160">Requirement</span></span> | <span data-ttu-id="26152-161">Valor</span><span class="sxs-lookup"><span data-stu-id="26152-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26152-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26152-162">Minimum supported client</span></span><br/> | <span data-ttu-id="26152-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26152-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26152-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26152-164">Minimum supported server</span></span><br/> | <span data-ttu-id="26152-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26152-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26152-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="26152-166">Namespace</span></span><br/>                | <span data-ttu-id="26152-167">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="26152-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26152-168">MOF</span><span class="sxs-lookup"><span data-stu-id="26152-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26152-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26152-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26152-170">DLL</span><span class="sxs-lookup"><span data-stu-id="26152-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26152-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26152-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26152-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="26152-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26152-173">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="26152-173">CIM\_Directory</span></span>](copyex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="26152-174">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="26152-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

