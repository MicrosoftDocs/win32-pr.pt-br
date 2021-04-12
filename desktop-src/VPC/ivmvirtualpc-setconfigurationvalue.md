---
title: Método setconfigurationvalue IVMVirtualPC (VPCCOMInterfaces. h)
description: Define o valor da definição de configuração especificada.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Método setconfigurationvalue Virtual PC
- Método setconfigurationvalue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método setconfiguraçãovalue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499604"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="7924d-106">Método IVMVirtualPC:: setconfigurationvalue</span><span class="sxs-lookup"><span data-stu-id="7924d-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="7924d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7924d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7924d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7924d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7924d-109">Define o valor da definição de configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="7924d-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="7924d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7924d-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="7924d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7924d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7924d-112">*preferenceKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7924d-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7924d-113">A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração por usuário (Options.xml em "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").</span><span class="sxs-lookup"><span data-stu-id="7924d-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7924d-114">As alterações devem ser feitas para Options.xml apenas usando **o método** setconfigurevalue.</span><span class="sxs-lookup"><span data-stu-id="7924d-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="7924d-115">Não há suporte para a alteração de Options.xml usando qualquer outro método.</span><span class="sxs-lookup"><span data-stu-id="7924d-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="7924d-116">*preferência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7924d-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7924d-117">O valor de preferência.</span><span class="sxs-lookup"><span data-stu-id="7924d-117">The preference value.</span></span> <span data-ttu-id="7924d-118">Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (booliano).</span><span class="sxs-lookup"><span data-stu-id="7924d-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7924d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7924d-119">Return value</span></span>

<span data-ttu-id="7924d-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7924d-120">This method can return one of these values.</span></span>



| <span data-ttu-id="7924d-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7924d-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="7924d-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="7924d-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7924d-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7924d-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="7924d-124">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7924d-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7924d-125"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7924d-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="7924d-126">O parâmetro *preferenceKey* ou *preferencevalue* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7924d-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="7924d-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="7924d-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="7924d-128">O parâmetro *preferenceKey* não é válido ou é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="7924d-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="7924d-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7924d-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="7924d-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7924d-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="7924d-131"><dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="7924d-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="7924d-132">O usuário atual não tem acesso suficiente ao arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="7924d-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="7924d-133"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7924d-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="7924d-134">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="7924d-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7924d-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="7924d-135">Remarks</span></span>

<span data-ttu-id="7924d-136">Os valores a seguir têm suporte para o parâmetro *preferenceKey* .</span><span class="sxs-lookup"><span data-stu-id="7924d-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="7924d-137">valor de *preferenceKey*</span><span class="sxs-lookup"><span data-stu-id="7924d-137">*preferenceKey* value</span></span>      | <span data-ttu-id="7924d-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="7924d-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="7924d-139">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7924d-139">Data type</span></span>            | <span data-ttu-id="7924d-140">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="7924d-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="7924d-141">" \_ tempo limite de ociosidade"</span><span class="sxs-lookup"><span data-stu-id="7924d-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="7924d-142">Número de segundos que vpc.exe deve aguardar antes de sair se não houver VMs ou aplicativos ativos usando as [interfaces do Windows Virtual PC](virtual-pc-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7924d-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="7924d-143">valores</span><span class="sxs-lookup"><span data-stu-id="7924d-143">"integer"</span></span><br/> | <span data-ttu-id="7924d-144">máximo</span><span class="sxs-lookup"><span data-stu-id="7924d-144">"30"</span></span><br/> |



 

<span data-ttu-id="7924d-145">Esse método fornece acesso de baixo nível a qualquer valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="7924d-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="7924d-146">Ele pode ser usado para definir valores de configuração para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="7924d-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="7924d-147">Tenha cuidado se você usar esse método para definir valores de configuração do sistema, porque nenhuma verificação de erro é executada no valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="7924d-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="7924d-148">Além disso, alguns valores de configuração não podem ser alterados enquanto uma máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="7924d-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="7924d-149">As chaves de configuração estão localizadas no arquivo "Options.xml" da máquina virtual no formato XML.</span><span class="sxs-lookup"><span data-stu-id="7924d-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="7924d-150">As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="7924d-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="7924d-151">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="7924d-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="7924d-152">Por exemplo, para definir o valor da \_ chave "tempo limite de ociosidade" localizado na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="7924d-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="7924d-153">A cadeia de caracteres de caminho *preferenceKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7924d-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="7924d-154">Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *preferenceKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="7924d-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="7924d-155">Por exemplo, para definir o valor da chave "golfe" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="7924d-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="7924d-156">A cadeia de caracteres de caminho *preferenceKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7924d-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="7924d-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7924d-157">Requirements</span></span>



| <span data-ttu-id="7924d-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="7924d-158">Requirement</span></span> | <span data-ttu-id="7924d-159">Valor</span><span class="sxs-lookup"><span data-stu-id="7924d-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7924d-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7924d-160">Minimum supported client</span></span><br/> | <span data-ttu-id="7924d-161">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7924d-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7924d-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7924d-162">Minimum supported server</span></span><br/> | <span data-ttu-id="7924d-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7924d-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7924d-164">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7924d-164">End of client support</span></span><br/>    | <span data-ttu-id="7924d-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7924d-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7924d-166">Produto</span><span class="sxs-lookup"><span data-stu-id="7924d-166">Product</span></span><br/>                  | <span data-ttu-id="7924d-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7924d-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7924d-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7924d-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="7924d-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7924d-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7924d-170">IID</span><span class="sxs-lookup"><span data-stu-id="7924d-170">IID</span></span><br/>                      | <span data-ttu-id="7924d-171">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="7924d-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7924d-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="7924d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7924d-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="7924d-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="7924d-174">**IVMVirtualMachine:: setconfigurationvalue**</span><span class="sxs-lookup"><span data-stu-id="7924d-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

