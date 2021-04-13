---
description: Descompacta o arquivo de dispositivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact. Esse método é herdado do \_ LogicalFile CIM.
ms.assetid: dfa53b75-56ef-4119-83b9-08b4371762c6
ms.tgt_platform: multiple
title: Método UncompressEx da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a760c31a2067c294ffb43064402ac179c5fba7c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501069"
---
# <a name="uncompressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="bde93-105">Método UncompressEx da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="bde93-105">UncompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="bde93-106">O método **UncompressEx** descompacta o arquivo de dispositivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="bde93-106">The **UncompressEx** method uncompresses the logical device file (or directory) specified in the object path.</span></span> <span data-ttu-id="bde93-107">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="bde93-107">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="bde93-108">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="bde93-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bde93-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bde93-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bde93-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bde93-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bde93-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="bde93-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bde93-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bde93-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bde93-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bde93-113">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="bde93-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bde93-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde93-115">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bde93-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bde93-116">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="bde93-116">String that represent the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="bde93-117">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="bde93-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="bde93-118">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bde93-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bde93-119">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para o método.</span><span class="sxs-lookup"><span data-stu-id="bde93-119">String that represents the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="bde93-120">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="bde93-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="bde93-121">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="bde93-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="bde93-122">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bde93-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bde93-123">Se **for true**, esse método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ dispositivo CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="bde93-123">If **TRUE**, this method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="bde93-124">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="bde93-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde93-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bde93-125">Return value</span></span>

<span data-ttu-id="bde93-126">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="bde93-126">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="bde93-127">0</span><span class="sxs-lookup"><span data-stu-id="bde93-127">0</span></span>

<span data-ttu-id="bde93-128">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="bde93-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-129">2</span><span class="sxs-lookup"><span data-stu-id="bde93-129">2</span></span>

<span data-ttu-id="bde93-130">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="bde93-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-131">8</span><span class="sxs-lookup"><span data-stu-id="bde93-131">8</span></span>

<span data-ttu-id="bde93-132">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="bde93-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-133">9</span><span class="sxs-lookup"><span data-stu-id="bde93-133">9</span></span>

<span data-ttu-id="bde93-134">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="bde93-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-135">10</span><span class="sxs-lookup"><span data-stu-id="bde93-135">10</span></span>

<span data-ttu-id="bde93-136">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="bde93-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-137">11</span><span class="sxs-lookup"><span data-stu-id="bde93-137">11</span></span>

<span data-ttu-id="bde93-138">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="bde93-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-139">12</span><span class="sxs-lookup"><span data-stu-id="bde93-139">12</span></span>

<span data-ttu-id="bde93-140">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="bde93-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-141">13</span><span class="sxs-lookup"><span data-stu-id="bde93-141">13</span></span>

<span data-ttu-id="bde93-142">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="bde93-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-143">14</span><span class="sxs-lookup"><span data-stu-id="bde93-143">14</span></span>

<span data-ttu-id="bde93-144">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="bde93-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-145">15</span><span class="sxs-lookup"><span data-stu-id="bde93-145">15</span></span>

<span data-ttu-id="bde93-146">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="bde93-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-147">16</span><span class="sxs-lookup"><span data-stu-id="bde93-147">16</span></span>

<span data-ttu-id="bde93-148">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="bde93-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-149">17</span><span class="sxs-lookup"><span data-stu-id="bde93-149">17</span></span>

<span data-ttu-id="bde93-150">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="bde93-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bde93-151">21</span><span class="sxs-lookup"><span data-stu-id="bde93-151">21</span></span>

<span data-ttu-id="bde93-152">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="bde93-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bde93-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="bde93-153">Remarks</span></span>

<span data-ttu-id="bde93-154">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="bde93-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="bde93-155">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="bde93-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="bde93-156">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bde93-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bde93-157">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bde93-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde93-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bde93-158">Requirements</span></span>



| <span data-ttu-id="bde93-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde93-159">Requirement</span></span> | <span data-ttu-id="bde93-160">Valor</span><span class="sxs-lookup"><span data-stu-id="bde93-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bde93-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bde93-161">Minimum supported client</span></span><br/> | <span data-ttu-id="bde93-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bde93-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bde93-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bde93-163">Minimum supported server</span></span><br/> | <span data-ttu-id="bde93-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bde93-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bde93-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="bde93-165">Namespace</span></span><br/>                | <span data-ttu-id="bde93-166">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bde93-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bde93-167">MOF</span><span class="sxs-lookup"><span data-stu-id="bde93-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bde93-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bde93-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bde93-169">DLL</span><span class="sxs-lookup"><span data-stu-id="bde93-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bde93-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bde93-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde93-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="bde93-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde93-172">\_Dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="bde93-172">CIM\_DeviceFile</span></span>](uncompressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="bde93-173">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="bde93-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

