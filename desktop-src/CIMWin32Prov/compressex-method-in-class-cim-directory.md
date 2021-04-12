---
description: O método CompressEx compacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método compress e é herdado de CIM \_ LogicalFile.
ms.assetid: 82a28a3b-b2e4-4834-b4a5-02ffe94f3fc7
ms.tgt_platform: multiple
title: Método CompressEx da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bebd729d87e012c3fce6dd2eb87b1c61ffa423a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500812"
---
# <a name="compressex-method-of-the-cim_directory-class"></a><span data-ttu-id="06087-104">Método CompressEx da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="06087-104">CompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="06087-105">O método **CompressEx** compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="06087-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06087-106">Esse método é uma versão estendida do método [**compress**](compress-method-in-class-cim-directory.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06087-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06087-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="06087-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06087-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="06087-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06087-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="06087-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="06087-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="06087-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="06087-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06087-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="06087-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06087-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06087-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06087-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06087-114">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="06087-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="06087-115">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="06087-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="06087-116">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06087-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06087-117">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="06087-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="06087-118">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="06087-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="06087-119">Se esse parâmetro for nulo, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="06087-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="06087-120">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06087-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06087-121">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ diretório CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="06087-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="06087-122">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="06087-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06087-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06087-123">Return value</span></span>

<span data-ttu-id="06087-124">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="06087-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="06087-125">0</span><span class="sxs-lookup"><span data-stu-id="06087-125">0</span></span>

<span data-ttu-id="06087-126">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="06087-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-127">2</span><span class="sxs-lookup"><span data-stu-id="06087-127">2</span></span>

<span data-ttu-id="06087-128">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="06087-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-129">8</span><span class="sxs-lookup"><span data-stu-id="06087-129">8</span></span>

<span data-ttu-id="06087-130">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="06087-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-131">9</span><span class="sxs-lookup"><span data-stu-id="06087-131">9</span></span>

<span data-ttu-id="06087-132">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="06087-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-133">10</span><span class="sxs-lookup"><span data-stu-id="06087-133">10</span></span>

<span data-ttu-id="06087-134">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="06087-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-135">11</span><span class="sxs-lookup"><span data-stu-id="06087-135">11</span></span>

<span data-ttu-id="06087-136">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="06087-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-137">12</span><span class="sxs-lookup"><span data-stu-id="06087-137">12</span></span>

<span data-ttu-id="06087-138">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="06087-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-139">13</span><span class="sxs-lookup"><span data-stu-id="06087-139">13</span></span>

<span data-ttu-id="06087-140">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="06087-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-141">14</span><span class="sxs-lookup"><span data-stu-id="06087-141">14</span></span>

<span data-ttu-id="06087-142">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="06087-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-143">15</span><span class="sxs-lookup"><span data-stu-id="06087-143">15</span></span>

<span data-ttu-id="06087-144">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="06087-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-145">16</span><span class="sxs-lookup"><span data-stu-id="06087-145">16</span></span>

<span data-ttu-id="06087-146">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="06087-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-147">17</span><span class="sxs-lookup"><span data-stu-id="06087-147">17</span></span>

<span data-ttu-id="06087-148">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="06087-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="06087-149">21</span><span class="sxs-lookup"><span data-stu-id="06087-149">21</span></span>

<span data-ttu-id="06087-150">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="06087-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06087-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="06087-151">Remarks</span></span>

<span data-ttu-id="06087-152">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="06087-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="06087-153">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="06087-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="06087-154">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="06087-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06087-155">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="06087-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06087-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06087-156">Requirements</span></span>



| <span data-ttu-id="06087-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="06087-157">Requirement</span></span> | <span data-ttu-id="06087-158">Valor</span><span class="sxs-lookup"><span data-stu-id="06087-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06087-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06087-159">Minimum supported client</span></span><br/> | <span data-ttu-id="06087-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06087-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06087-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06087-161">Minimum supported server</span></span><br/> | <span data-ttu-id="06087-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06087-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06087-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="06087-163">Namespace</span></span><br/>                | <span data-ttu-id="06087-164">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="06087-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06087-165">MOF</span><span class="sxs-lookup"><span data-stu-id="06087-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06087-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06087-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06087-167">DLL</span><span class="sxs-lookup"><span data-stu-id="06087-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06087-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06087-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06087-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="06087-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06087-170">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="06087-170">CIM\_Directory</span></span>](compressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="06087-171">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="06087-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

