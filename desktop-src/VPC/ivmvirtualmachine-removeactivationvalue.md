---
title: Método IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Remove o valor da configuração de ativação especificada para esta máquina virtual.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- RemoveActivationValue do método virtual PC
- Método RemoveActivationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009461"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="b4235-106">Método IVMVirtualMachine:: RemoveActivationValue</span><span class="sxs-lookup"><span data-stu-id="b4235-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="b4235-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b4235-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b4235-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b4235-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b4235-109">Remove o valor da configuração de ativação especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b4235-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4235-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4235-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="b4235-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4235-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4235-112">*activationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4235-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4235-113">A chave usada para identificar o valor de ativação, como armazenado no \* arquivo ". vmc".</span><span class="sxs-lookup"><span data-stu-id="b4235-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4235-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4235-114">Return value</span></span>

<span data-ttu-id="b4235-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b4235-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b4235-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b4235-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="b4235-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4235-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4235-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b4235-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="b4235-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4235-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="b4235-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b4235-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="b4235-121">O parâmetro é **nulo** ou está vazio.</span><span class="sxs-lookup"><span data-stu-id="b4235-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="b4235-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b4235-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="b4235-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="b4235-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="b4235-124"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="b4235-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="b4235-125">A preferência não foi encontrada ou essa configuração não tem ativação válida.</span><span class="sxs-lookup"><span data-stu-id="b4235-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="b4235-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b4235-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="b4235-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b4235-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b4235-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4235-128">Remarks</span></span>

<span data-ttu-id="b4235-129">Esse método fornece acesso de baixo nível a qualquer valor de ativação.</span><span class="sxs-lookup"><span data-stu-id="b4235-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="b4235-130">Ele pode ser usado para remover valores de ativação para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="b4235-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="b4235-131">Tenha cuidado ao usar esse método para remover valores de ativação do sistema, já que alguns valores não podem ser alterados enquanto a máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="b4235-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="b4235-132">Quando uma máquina virtual é iniciada, uma cópia é feita de seus valores de configuração, que se torna seu conjunto de valores de ativação.</span><span class="sxs-lookup"><span data-stu-id="b4235-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="b4235-133">Os valores de ativação são mantidos até que a máquina virtual seja desligada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="b4235-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="b4235-134">Observe que o Windows Virtual PC pode usar apenas a configuração para armazenar valores para determinadas chaves, ou seja, o valor de ativação pode nunca ser usado.</span><span class="sxs-lookup"><span data-stu-id="b4235-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="b4235-135">A sessão da máquina virtual deve estar em execução antes que qualquer valor de ativação possa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="b4235-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="b4235-136">As chaves de ativação são armazenadas internamente de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="b4235-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="b4235-137">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="b4235-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="b4235-138">Por exemplo, para remover o valor da \_ chave "ação padrão" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="b4235-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="b4235-139">A cadeia de caracteres de caminho *activationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b4235-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="b4235-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4235-140">Requirements</span></span>



| <span data-ttu-id="b4235-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4235-141">Requirement</span></span> | <span data-ttu-id="b4235-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b4235-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4235-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4235-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b4235-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b4235-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4235-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4235-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b4235-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b4235-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b4235-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b4235-147">End of client support</span></span><br/>    | <span data-ttu-id="b4235-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4235-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b4235-149">Produto</span><span class="sxs-lookup"><span data-stu-id="b4235-149">Product</span></span><br/>                  | <span data-ttu-id="b4235-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b4235-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b4235-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4235-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4235-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4235-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b4235-153">IID</span><span class="sxs-lookup"><span data-stu-id="b4235-153">IID</span></span><br/>                      | <span data-ttu-id="b4235-154">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b4235-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b4235-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4235-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4235-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b4235-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

