---
title: Método getactivationvalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o valor da configuração de ativação especificada para esta máquina virtual.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- PC virtual do método getactivationvalue
- Método getactivavalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, getactivationvalue método
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294747"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="40c34-106">Método IVMVirtualMachine:: getactivationvalue</span><span class="sxs-lookup"><span data-stu-id="40c34-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="40c34-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40c34-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40c34-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40c34-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40c34-109">Recupera o valor da configuração de ativação especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="40c34-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c34-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40c34-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="40c34-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40c34-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c34-112">*activationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40c34-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c34-113">A chave usada para identificar o valor de ativação, como armazenado no \* arquivo ". vmc".</span><span class="sxs-lookup"><span data-stu-id="40c34-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="40c34-114">*activationvalue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="40c34-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="40c34-115">O valor de ativação.</span><span class="sxs-lookup"><span data-stu-id="40c34-115">The activation value.</span></span> <span data-ttu-id="40c34-116">Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ i4** (Integer) ou **VT \_ bool** (booliano).</span><span class="sxs-lookup"><span data-stu-id="40c34-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c34-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40c34-117">Return value</span></span>

<span data-ttu-id="40c34-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="40c34-118">This method can return one of these values.</span></span>



| <span data-ttu-id="40c34-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="40c34-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="40c34-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="40c34-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40c34-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40c34-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="40c34-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="40c34-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="40c34-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="40c34-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="40c34-124">O parâmetro *activationKey* é **nulo** ou está vazio.</span><span class="sxs-lookup"><span data-stu-id="40c34-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="40c34-125"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="40c34-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="40c34-126">O parâmetro *activationvalue* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="40c34-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="40c34-127"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40c34-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="40c34-128">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="40c34-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="40c34-129"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="40c34-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="40c34-130">A preferência não foi encontrada ou essa configuração não tem ativação válida.</span><span class="sxs-lookup"><span data-stu-id="40c34-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="40c34-131"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="40c34-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="40c34-132">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="40c34-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="40c34-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="40c34-133">Remarks</span></span>

<span data-ttu-id="40c34-134">Esse método fornece acesso de baixo nível a qualquer valor de ativação.</span><span class="sxs-lookup"><span data-stu-id="40c34-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="40c34-135">Ele pode ser usado para definir valores de ativação para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="40c34-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="40c34-136">Quando uma máquina virtual é iniciada, uma cópia é feita de seus valores de configuração, que se torna seu conjunto de valores de ativação.</span><span class="sxs-lookup"><span data-stu-id="40c34-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="40c34-137">Os valores de ativação são mantidos até que a máquina virtual seja desligada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="40c34-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="40c34-138">Observe que o Windows Virtual PC pode usar apenas a configuração para armazenar valores para determinadas chaves, ou seja, o valor de ativação pode nunca ser usado.</span><span class="sxs-lookup"><span data-stu-id="40c34-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="40c34-139">As chaves de ativação são armazenadas internamente de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="40c34-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="40c34-140">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="40c34-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="40c34-141">Por exemplo, para ler o valor da \_ chave "ação padrão" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="40c34-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="40c34-142">A cadeia de caracteres de caminho *activationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="40c34-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="40c34-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40c34-143">Requirements</span></span>



| <span data-ttu-id="40c34-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="40c34-144">Requirement</span></span> | <span data-ttu-id="40c34-145">Valor</span><span class="sxs-lookup"><span data-stu-id="40c34-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c34-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c34-146">Minimum supported client</span></span><br/> | <span data-ttu-id="40c34-147">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="40c34-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40c34-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c34-148">Minimum supported server</span></span><br/> | <span data-ttu-id="40c34-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="40c34-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40c34-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="40c34-150">End of client support</span></span><br/>    | <span data-ttu-id="40c34-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40c34-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40c34-152">Produto</span><span class="sxs-lookup"><span data-stu-id="40c34-152">Product</span></span><br/>                  | <span data-ttu-id="40c34-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40c34-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40c34-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40c34-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c34-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40c34-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40c34-156">IID</span><span class="sxs-lookup"><span data-stu-id="40c34-156">IID</span></span><br/>                      | <span data-ttu-id="40c34-157">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="40c34-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="40c34-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="40c34-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c34-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="40c34-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

