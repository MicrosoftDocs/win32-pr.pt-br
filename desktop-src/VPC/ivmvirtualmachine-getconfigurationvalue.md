---
title: Método getconfigurationvalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o valor da definição de configuração especificada para esta máquina virtual.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- PC virtual do método getconfigurationvalue
- Método getconfigurationvalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método getconfigurationvalue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369686"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="8b73d-106">Método IVMVirtualMachine:: getconfigurationvalue</span><span class="sxs-lookup"><span data-stu-id="8b73d-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="8b73d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8b73d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8b73d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8b73d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8b73d-109">Recupera o valor da definição de configuração especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b73d-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b73d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b73d-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="8b73d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b73d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b73d-112">*configurationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b73d-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b73d-113">A chave usada para identificar o valor de configuração como armazenado no \* arquivo ". vmc".</span><span class="sxs-lookup"><span data-stu-id="8b73d-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="8b73d-114">*configuração* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8b73d-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8b73d-115">O valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="8b73d-115">The configuration value.</span></span> <span data-ttu-id="8b73d-116">Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ i4** (Integer) ou **VT \_ bool** (booliano).</span><span class="sxs-lookup"><span data-stu-id="8b73d-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b73d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b73d-117">Return value</span></span>

<span data-ttu-id="8b73d-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8b73d-118">This method can return one of these values.</span></span>



| <span data-ttu-id="8b73d-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8b73d-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="8b73d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b73d-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b73d-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b73d-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="8b73d-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8b73d-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="8b73d-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8b73d-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="8b73d-124">O parâmetro *configurationKey* é **nulo** ou está vazio.</span><span class="sxs-lookup"><span data-stu-id="8b73d-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="8b73d-125"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8b73d-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="8b73d-126">O parâmetro *ConfigurationValue* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8b73d-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8b73d-127"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8b73d-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="8b73d-128">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8b73d-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="8b73d-129"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="8b73d-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="8b73d-130">A preferência não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="8b73d-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="8b73d-131"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8b73d-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="8b73d-132">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8b73d-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="8b73d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b73d-133">Remarks</span></span>

<span data-ttu-id="8b73d-134">Esse método fornece acesso de baixo nível a qualquer valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="8b73d-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="8b73d-135">Ele pode ser usado para ler valores de configuração para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="8b73d-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="8b73d-136">As chaves de configuração estão localizadas no arquivo " \* . vmc" da máquina virtual no formato XML.</span><span class="sxs-lookup"><span data-stu-id="8b73d-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="8b73d-137">As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="8b73d-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="8b73d-138">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="8b73d-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="8b73d-139">Por exemplo, para ler o valor da chave "tamanho da RAM \_ " localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="8b73d-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="8b73d-140">A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8b73d-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="8b73d-141">Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *configurationKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="8b73d-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="8b73d-142">Por exemplo, para ler o valor da chave "Absolute" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="8b73d-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="8b73d-143">A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8b73d-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="8b73d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b73d-144">Requirements</span></span>



| <span data-ttu-id="8b73d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b73d-145">Requirement</span></span> | <span data-ttu-id="8b73d-146">Valor</span><span class="sxs-lookup"><span data-stu-id="8b73d-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b73d-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b73d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8b73d-148">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8b73d-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b73d-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b73d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8b73d-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8b73d-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8b73d-151">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8b73d-151">End of client support</span></span><br/>    | <span data-ttu-id="8b73d-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b73d-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8b73d-153">Produto</span><span class="sxs-lookup"><span data-stu-id="8b73d-153">Product</span></span><br/>                  | <span data-ttu-id="8b73d-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8b73d-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8b73d-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b73d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b73d-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b73d-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8b73d-157">IID</span><span class="sxs-lookup"><span data-stu-id="8b73d-157">IID</span></span><br/>                      | <span data-ttu-id="8b73d-158">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8b73d-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8b73d-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b73d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b73d-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8b73d-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

