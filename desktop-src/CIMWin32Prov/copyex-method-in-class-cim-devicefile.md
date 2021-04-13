---
description: Copia o arquivo de dispositivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro FileName.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: Método CopyEx da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370439"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="08a3b-103">Método CopyEx da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="08a3b-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="08a3b-104">O método **CopyEx** copia o arquivo de dispositivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="08a3b-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="08a3b-105">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="08a3b-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="08a3b-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="08a3b-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="08a3b-107">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="08a3b-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08a3b-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="08a3b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08a3b-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="08a3b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08a3b-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="08a3b-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="08a3b-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="08a3b-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="08a3b-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08a3b-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="08a3b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08a3b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a3b-114">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08a3b-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a3b-115">Nome totalmente qualificado do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="08a3b-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="08a3b-116">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="08a3b-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="08a3b-117">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="08a3b-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08a3b-118">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="08a3b-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="08a3b-119">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="08a3b-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="08a3b-120">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08a3b-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a3b-121">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="08a3b-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="08a3b-122">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="08a3b-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="08a3b-123">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="08a3b-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="08a3b-124">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08a3b-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a3b-125">Se for TRUE, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ dispositivo CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="08a3b-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="08a3b-126">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="08a3b-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a3b-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08a3b-127">Return value</span></span>

<span data-ttu-id="08a3b-128">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="08a3b-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-129">0</span><span class="sxs-lookup"><span data-stu-id="08a3b-129">0</span></span>

<span data-ttu-id="08a3b-130">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="08a3b-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-131">2</span><span class="sxs-lookup"><span data-stu-id="08a3b-131">2</span></span>

<span data-ttu-id="08a3b-132">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="08a3b-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-133">8</span><span class="sxs-lookup"><span data-stu-id="08a3b-133">8</span></span>

<span data-ttu-id="08a3b-134">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="08a3b-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-135">9</span><span class="sxs-lookup"><span data-stu-id="08a3b-135">9</span></span>

<span data-ttu-id="08a3b-136">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="08a3b-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-137">10</span><span class="sxs-lookup"><span data-stu-id="08a3b-137">10</span></span>

<span data-ttu-id="08a3b-138">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="08a3b-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-139">11</span><span class="sxs-lookup"><span data-stu-id="08a3b-139">11</span></span>

<span data-ttu-id="08a3b-140">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="08a3b-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-141">12</span><span class="sxs-lookup"><span data-stu-id="08a3b-141">12</span></span>

<span data-ttu-id="08a3b-142">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="08a3b-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-143">13</span><span class="sxs-lookup"><span data-stu-id="08a3b-143">13</span></span>

<span data-ttu-id="08a3b-144">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="08a3b-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-145">14</span><span class="sxs-lookup"><span data-stu-id="08a3b-145">14</span></span>

<span data-ttu-id="08a3b-146">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="08a3b-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-147">15</span><span class="sxs-lookup"><span data-stu-id="08a3b-147">15</span></span>

<span data-ttu-id="08a3b-148">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="08a3b-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-149">16</span><span class="sxs-lookup"><span data-stu-id="08a3b-149">16</span></span>

<span data-ttu-id="08a3b-150">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="08a3b-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-151">17</span><span class="sxs-lookup"><span data-stu-id="08a3b-151">17</span></span>

<span data-ttu-id="08a3b-152">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="08a3b-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="08a3b-153">21</span><span class="sxs-lookup"><span data-stu-id="08a3b-153">21</span></span>

<span data-ttu-id="08a3b-154">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="08a3b-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08a3b-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="08a3b-155">Remarks</span></span>

<span data-ttu-id="08a3b-156">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="08a3b-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="08a3b-157">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="08a3b-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="08a3b-158">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="08a3b-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08a3b-159">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="08a3b-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a3b-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08a3b-160">Requirements</span></span>



| <span data-ttu-id="08a3b-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a3b-161">Requirement</span></span> | <span data-ttu-id="08a3b-162">Valor</span><span class="sxs-lookup"><span data-stu-id="08a3b-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08a3b-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08a3b-163">Minimum supported client</span></span><br/> | <span data-ttu-id="08a3b-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08a3b-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08a3b-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08a3b-165">Minimum supported server</span></span><br/> | <span data-ttu-id="08a3b-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08a3b-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08a3b-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="08a3b-167">Namespace</span></span><br/>                | <span data-ttu-id="08a3b-168">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="08a3b-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08a3b-169">MOF</span><span class="sxs-lookup"><span data-stu-id="08a3b-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08a3b-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08a3b-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08a3b-171">DLL</span><span class="sxs-lookup"><span data-stu-id="08a3b-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a3b-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a3b-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a3b-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="08a3b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a3b-174">\_Dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="08a3b-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="08a3b-175">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="08a3b-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

