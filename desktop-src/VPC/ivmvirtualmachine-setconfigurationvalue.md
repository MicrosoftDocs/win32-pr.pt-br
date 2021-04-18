---
title: Método setconfigurationvalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Define o valor da definição de configuração especificada para esta VM (máquina virtual).
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Método setconfigurationvalue Virtual PC
- Método setconfigurationvalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método setconfiguraçãovalue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105807185"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="d796d-106">Método IVMVirtualMachine:: setconfigurationvalue</span><span class="sxs-lookup"><span data-stu-id="d796d-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="d796d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d796d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d796d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d796d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d796d-109">Define o valor da definição de configuração especificada para esta VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="d796d-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d796d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d796d-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="d796d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d796d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d796d-112">*configurationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d796d-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d796d-113">A chave usada para identificar o valor de configuração como armazenado no \* arquivo ". vmc".</span><span class="sxs-lookup"><span data-stu-id="d796d-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d796d-114">As alterações devem ser feitas em " \* . vmc" usando apenas  o método setconfigurevalue.</span><span class="sxs-lookup"><span data-stu-id="d796d-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="d796d-115">\*Não há suporte para alterar ". vmc" usando qualquer outro método.</span><span class="sxs-lookup"><span data-stu-id="d796d-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="d796d-116">*configuração* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d796d-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d796d-117">O valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="d796d-117">The configuration value.</span></span> <span data-ttu-id="d796d-118">Esse valor Cay ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (booliano).</span><span class="sxs-lookup"><span data-stu-id="d796d-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d796d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d796d-119">Return value</span></span>

<span data-ttu-id="d796d-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d796d-120">This method can return one of these values.</span></span>



| <span data-ttu-id="d796d-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d796d-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="d796d-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d796d-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d796d-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d796d-124">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d796d-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d796d-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="d796d-126">O parâmetro *configurationKey* é **nulo** ou vazio ou o parâmetro *ConfigurationValue* não é um tipo Variant válido.</span><span class="sxs-lookup"><span data-stu-id="d796d-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="d796d-127"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d796d-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d796d-128">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="d796d-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d796d-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="d796d-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d796d-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="d796d-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d796d-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="d796d-131">Remarks</span></span>

<span data-ttu-id="d796d-132">Os valores a seguir têm suporte para o parâmetro *configurationKey* .</span><span class="sxs-lookup"><span data-stu-id="d796d-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="d796d-133">valor de *configurationKey*</span><span class="sxs-lookup"><span data-stu-id="d796d-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="d796d-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="d796d-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="d796d-135">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d796d-135">Data type</span></span>            | <span data-ttu-id="d796d-136">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d796d-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="d796d-137">"sincronização de hardware/BIOS/horário \_ \_ na \_ inicialização"</span><span class="sxs-lookup"><span data-stu-id="d796d-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="d796d-138">"true" se o relógio CMOS da VM for sincronizado com o relógio do host na inicialização; caso contrário, "false".</span><span class="sxs-lookup"><span data-stu-id="d796d-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="d796d-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="d796d-139">"boolean"</span></span><br/> | <span data-ttu-id="d796d-140">"true"</span><span class="sxs-lookup"><span data-stu-id="d796d-140">"true"</span></span><br/> |
| <span data-ttu-id="d796d-141">"integração/Microsoft/sincronização de horário do host \_ \_ /habilitado" "</span><span class="sxs-lookup"><span data-stu-id="d796d-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="d796d-142">"verdadeiro" se a sincronização de tempo do host estiver habilitada nos componentes de integração; caso contrário, "false".</span><span class="sxs-lookup"><span data-stu-id="d796d-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="d796d-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="d796d-143">"boolean"</span></span><br/> | <span data-ttu-id="d796d-144">"true"</span><span class="sxs-lookup"><span data-stu-id="d796d-144">"true"</span></span><br/> |
| <span data-ttu-id="d796d-145">"opções da interface do usuário \_ /publicação automática de \_ aplicativo \_ "</span><span class="sxs-lookup"><span data-stu-id="d796d-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="d796d-146">"verdadeiro" se a publicação automática de aplicativos estiver habilitada nos componentes de integração; caso contrário, "false".</span><span class="sxs-lookup"><span data-stu-id="d796d-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="d796d-147">Isso também é chamado de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="d796d-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d796d-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="d796d-148">"boolean"</span></span><br/> | <span data-ttu-id="d796d-149">"true"</span><span class="sxs-lookup"><span data-stu-id="d796d-149">"true"</span></span><br/> |
| <span data-ttu-id="d796d-150">"opções de interface do usuário \_ /segundos \_ para \_ salvar"</span><span class="sxs-lookup"><span data-stu-id="d796d-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="d796d-151">Número de segundos a aguardar antes de salvar a VM depois que todos os aplicativos forem fechados.</span><span class="sxs-lookup"><span data-stu-id="d796d-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="d796d-152">No entanto, os valores abaixo de 20 e mais de 4.294.968 têm significados especiais.</span><span class="sxs-lookup"><span data-stu-id="d796d-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="d796d-153">Para obter detalhes, consulte a lista a seguir</span><span class="sxs-lookup"><span data-stu-id="d796d-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="d796d-154"><dt><span id="0"></span>0</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="d796d-155">Nunca salve a VM.</span><span class="sxs-lookup"><span data-stu-id="d796d-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="d796d-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="d796d-157">Aguarde 20 segundos antes de salvar a VM.</span><span class="sxs-lookup"><span data-stu-id="d796d-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="d796d-158"><dt><span id="214_294_967"></span>21 4.294.967</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="d796d-159">Aguarde o número especificado de segundos antes de salvar a VM.</span><span class="sxs-lookup"><span data-stu-id="d796d-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="d796d-160"><dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="d796d-161">Aguarde 4.294.968 segundos antes de salvar a VM.</span><span class="sxs-lookup"><span data-stu-id="d796d-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="d796d-162">valores</span><span class="sxs-lookup"><span data-stu-id="d796d-162">"integer"</span></span><br/> | <span data-ttu-id="d796d-163">300</span><span class="sxs-lookup"><span data-stu-id="d796d-163">300</span></span><br/>    |



 

<span data-ttu-id="d796d-164">Esse método fornece acesso de baixo nível a qualquer valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="d796d-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="d796d-165">Ele pode ser usado para definir valores de configuração para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d796d-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="d796d-166">Tenha cuidado se você usar esse método para definir valores de configuração do sistema, porque nenhuma verificação de erro é executada no valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="d796d-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="d796d-167">Além disso, alguns valores de configuração não podem ser alterados enquanto a máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="d796d-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="d796d-168">As chaves de configuração estão localizadas no arquivo " \* . vmc" da máquina virtual no formato XML.</span><span class="sxs-lookup"><span data-stu-id="d796d-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="d796d-169">As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows.</span><span class="sxs-lookup"><span data-stu-id="d796d-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="d796d-170">Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.</span><span class="sxs-lookup"><span data-stu-id="d796d-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="d796d-171">Por exemplo, para definir o valor da chave "tamanho da RAM \_ " localizado na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="d796d-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="d796d-172">A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d796d-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="d796d-173">Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *configurationKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="d796d-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="d796d-174">Por exemplo, para definir o valor da chave "golfe" localizada na seguinte árvore de chave:</span><span class="sxs-lookup"><span data-stu-id="d796d-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="d796d-175">A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d796d-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="d796d-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d796d-176">Requirements</span></span>



| <span data-ttu-id="d796d-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="d796d-177">Requirement</span></span> | <span data-ttu-id="d796d-178">Valor</span><span class="sxs-lookup"><span data-stu-id="d796d-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d796d-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d796d-179">Minimum supported client</span></span><br/> | <span data-ttu-id="d796d-180">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d796d-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d796d-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d796d-181">Minimum supported server</span></span><br/> | <span data-ttu-id="d796d-182">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d796d-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d796d-183">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d796d-183">End of client support</span></span><br/>    | <span data-ttu-id="d796d-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d796d-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d796d-185">Produto</span><span class="sxs-lookup"><span data-stu-id="d796d-185">Product</span></span><br/>                  | <span data-ttu-id="d796d-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d796d-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d796d-187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d796d-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="d796d-188"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d796d-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d796d-189">IID</span><span class="sxs-lookup"><span data-stu-id="d796d-189">IID</span></span><br/>                      | <span data-ttu-id="d796d-190">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d796d-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d796d-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="d796d-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d796d-192">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d796d-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="d796d-193">**IVMVirtualPC:: setconfigurationvalue**</span><span class="sxs-lookup"><span data-stu-id="d796d-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

