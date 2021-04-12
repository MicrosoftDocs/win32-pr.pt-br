---
title: Método setactivavalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Define o valor da configuração de ativação especificada para esta máquina virtual.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Método setactivavalue Virtual PC
- Método setactivavalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método setactivavalue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455685"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="bcaca-106">Método IVMVirtualMachine:: setactivationvalue</span><span class="sxs-lookup"><span data-stu-id="bcaca-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="bcaca-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bcaca-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bcaca-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bcaca-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bcaca-109">Define o valor da configuração de ativação especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bcaca-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcaca-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcaca-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="bcaca-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcaca-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcaca-112">*activationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bcaca-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcaca-113">A chave usada para identificar o valor de ativação, como armazenado no \* arquivo ". vmc".</span><span class="sxs-lookup"><span data-stu-id="bcaca-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="bcaca-114">*activationvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bcaca-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcaca-115">O valor de ativação.</span><span class="sxs-lookup"><span data-stu-id="bcaca-115">The activation value.</span></span> <span data-ttu-id="bcaca-116">Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (booliano).</span><span class="sxs-lookup"><span data-stu-id="bcaca-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcaca-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcaca-117">Return value</span></span>

<span data-ttu-id="bcaca-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bcaca-118">This method can return one of these values.</span></span>



| <span data-ttu-id="bcaca-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bcaca-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="bcaca-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="bcaca-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcaca-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bcaca-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="bcaca-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bcaca-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="bcaca-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bcaca-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="bcaca-124">O parâmetro *activationKey* é **nulo** ou vazio, ou o parâmetro *activationvalue* não é um tipo de variante válido.</span><span class="sxs-lookup"><span data-stu-id="bcaca-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="bcaca-125"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bcaca-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="bcaca-126">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="bcaca-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="bcaca-127"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="bcaca-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="bcaca-128">A configuração não tem ativação válida.</span><span class="sxs-lookup"><span data-stu-id="bcaca-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="bcaca-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="bcaca-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="bcaca-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="bcaca-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="bcaca-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcaca-131">Remarks</span></span>

<span data-ttu-id="bcaca-132">Esse método fornece acesso de baixo nível a qualquer valor de ativação.</span><span class="sxs-lookup"><span data-stu-id="bcaca-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="bcaca-133">Ele pode ser usado para definir valores de ativação para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="bcaca-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="bcaca-134">Tenha cuidado ao usar esse método para definir valores de ativação do sistema, pois nenhuma verificação de erro é executada no valor de ativação.</span><span class="sxs-lookup"><span data-stu-id="bcaca-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="bcaca-135">Além disso, alguns valores de ativação não podem ser alterados enquanto a máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="bcaca-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="bcaca-136">Quando uma máquina virtual é iniciada, uma cópia é feita de seus valores de configuração, que se torna seu conjunto de valores de ativação.</span><span class="sxs-lookup"><span data-stu-id="bcaca-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="bcaca-137">Os valores de ativação são mantidos até que a máquina virtual seja desligada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="bcaca-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="bcaca-138">Observe que o Windows Virtual PC pode usar apenas a configuração para armazenar valores para determinadas chaves, ou seja, o valor de ativação pode nunca ser usado.</span><span class="sxs-lookup"><span data-stu-id="bcaca-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="bcaca-139">A sessão da máquina virtual deve estar em execução antes que qualquer valor de ativação possa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bcaca-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="bcaca-140">As chaves de ativação são armazenadas internamente de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="bcaca-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="bcaca-141">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="bcaca-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="bcaca-142">Por exemplo, para definir o valor da \_ chave "ação padrão" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="bcaca-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="bcaca-143">A cadeia de caracteres de caminho *activationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bcaca-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="bcaca-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcaca-144">Requirements</span></span>



| <span data-ttu-id="bcaca-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcaca-145">Requirement</span></span> | <span data-ttu-id="bcaca-146">Valor</span><span class="sxs-lookup"><span data-stu-id="bcaca-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcaca-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcaca-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bcaca-148">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bcaca-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcaca-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcaca-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bcaca-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bcaca-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bcaca-151">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bcaca-151">End of client support</span></span><br/>    | <span data-ttu-id="bcaca-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bcaca-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bcaca-153">Produto</span><span class="sxs-lookup"><span data-stu-id="bcaca-153">Product</span></span><br/>                  | <span data-ttu-id="bcaca-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bcaca-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bcaca-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcaca-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcaca-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcaca-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bcaca-157">IID</span><span class="sxs-lookup"><span data-stu-id="bcaca-157">IID</span></span><br/>                      | <span data-ttu-id="bcaca-158">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="bcaca-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bcaca-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcaca-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcaca-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="bcaca-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

