---
title: Método IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Remove o valor da definição de configuração especificada para esta máquina virtual.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- RemoveConfigurationValue do método virtual PC
- Método RemoveConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455569"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="230b6-106">Método IVMVirtualMachine:: RemoveConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="230b6-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="230b6-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="230b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="230b6-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="230b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="230b6-109">Remove o valor da definição de configuração especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="230b6-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="230b6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="230b6-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="230b6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="230b6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230b6-112">*configurationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="230b6-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b6-113">A chave usada para identificar o valor de configuração como armazenado no \* arquivo ". vmc".</span><span class="sxs-lookup"><span data-stu-id="230b6-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230b6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="230b6-114">Return value</span></span>

<span data-ttu-id="230b6-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="230b6-115">This method can return one of these values.</span></span>



| <span data-ttu-id="230b6-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="230b6-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="230b6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="230b6-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="230b6-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="230b6-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="230b6-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="230b6-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="230b6-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="230b6-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="230b6-121">O parâmetro é **nulo** ou está vazio.</span><span class="sxs-lookup"><span data-stu-id="230b6-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="230b6-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="230b6-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="230b6-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="230b6-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="230b6-124"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="230b6-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="230b6-125">A preferência não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="230b6-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="230b6-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="230b6-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="230b6-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="230b6-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="230b6-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="230b6-128">Remarks</span></span>

<span data-ttu-id="230b6-129">Esse método fornece acesso de baixo nível a qualquer valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="230b6-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="230b6-130">Ele pode ser usado para remover valores de configuração para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="230b6-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="230b6-131">Tenha cuidado ao usar esse método para remover valores de configuração do sistema, já que alguns valores não podem ser alterados enquanto a máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="230b6-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="230b6-132">As chaves de configuração estão localizadas no arquivo " \* . vmc" da máquina virtual no formato XML.</span><span class="sxs-lookup"><span data-stu-id="230b6-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="230b6-133">As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="230b6-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="230b6-134">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="230b6-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="230b6-135">Por exemplo, para remover o valor da chave "tamanho da RAM \_ " localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="230b6-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="230b6-136">A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="230b6-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="230b6-137">Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *configurationKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="230b6-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="230b6-138">Por exemplo, para remover o valor da chave "Absolute" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="230b6-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="230b6-139">A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="230b6-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="230b6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230b6-140">Requirements</span></span>



| <span data-ttu-id="230b6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="230b6-141">Requirement</span></span> | <span data-ttu-id="230b6-142">Valor</span><span class="sxs-lookup"><span data-stu-id="230b6-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="230b6-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="230b6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="230b6-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="230b6-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="230b6-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="230b6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="230b6-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="230b6-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="230b6-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="230b6-147">End of client support</span></span><br/>    | <span data-ttu-id="230b6-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="230b6-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="230b6-149">Produto</span><span class="sxs-lookup"><span data-stu-id="230b6-149">Product</span></span><br/>                  | <span data-ttu-id="230b6-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="230b6-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="230b6-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="230b6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="230b6-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="230b6-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="230b6-153">IID</span><span class="sxs-lookup"><span data-stu-id="230b6-153">IID</span></span><br/>                      | <span data-ttu-id="230b6-154">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="230b6-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="230b6-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="230b6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230b6-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="230b6-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

