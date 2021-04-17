---
description: Obtém os dados brutos de uma estrutura E-EDID (dados de identificação de exibição estendida) avançada da VESA (Standard Electronics data Identification) que define as configurações ideais para configurar um monitor.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Método WmiGetMonitorRawEEdidV1Block da classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765259"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="31cd5-103">Método WmiGetMonitorRawEEdidV1Block da classe WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="31cd5-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="31cd5-104">O método **WmiGetMonitorRawEEdidV1Block** Obtém os dados brutos de uma estrutura E-EDID (dados de identificação de exibição estendida) avançada da VESA (Standard Electronics data Identification) que define as configurações ideais para configurar um monitor.</span><span class="sxs-lookup"><span data-stu-id="31cd5-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cd5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31cd5-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="31cd5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31cd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31cd5-107">*Blockid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31cd5-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31cd5-108">A identidade do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="31cd5-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="31cd5-109">*BlockType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31cd5-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31cd5-110">Tipo de bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="31cd5-110">Type of data block.</span></span> <span data-ttu-id="31cd5-111">A tabela a seguir lista os possíveis valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="31cd5-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="31cd5-112">Valor</span><span class="sxs-lookup"><span data-stu-id="31cd5-112">Value</span></span>                                                                                 | <span data-ttu-id="31cd5-113">Significado</span><span class="sxs-lookup"><span data-stu-id="31cd5-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="31cd5-114"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="31cd5-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="31cd5-115">Não Inicializado</span><span class="sxs-lookup"><span data-stu-id="31cd5-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="31cd5-116"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="31cd5-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="31cd5-117">Bloco base EDID</span><span class="sxs-lookup"><span data-stu-id="31cd5-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="31cd5-118"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="31cd5-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="31cd5-119">Mapa de bloco EDID</span><span class="sxs-lookup"><span data-stu-id="31cd5-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="31cd5-120"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="31cd5-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="31cd5-121">Outro</span><span class="sxs-lookup"><span data-stu-id="31cd5-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="31cd5-122">*BlockContent* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31cd5-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31cd5-123">Uma matriz de 128 bytes que contém o conteúdo de bloco bruto.</span><span class="sxs-lookup"><span data-stu-id="31cd5-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31cd5-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31cd5-124">Return value</span></span>

<span data-ttu-id="31cd5-125">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="31cd5-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="31cd5-126">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="31cd5-126">Any other number indicates an error.</span></span> <span data-ttu-id="31cd5-127">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="31cd5-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="31cd5-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31cd5-128">Examples</span></span>

<span data-ttu-id="31cd5-129">O exemplo de código a seguir recupera os blocos EDID de qualquer exibição como matrizes de bits de 128 brutos.</span><span class="sxs-lookup"><span data-stu-id="31cd5-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="31cd5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31cd5-130">Requirements</span></span>



| <span data-ttu-id="31cd5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="31cd5-131">Requirement</span></span> | <span data-ttu-id="31cd5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="31cd5-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31cd5-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31cd5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="31cd5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31cd5-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="31cd5-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31cd5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="31cd5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31cd5-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="31cd5-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="31cd5-137">Namespace</span></span><br/>                | <span data-ttu-id="31cd5-138">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="31cd5-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="31cd5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="31cd5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31cd5-140"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31cd5-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="31cd5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="31cd5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31cd5-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31cd5-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31cd5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="31cd5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cd5-144">**WmiMonitorDescriptorMethods**</span><span class="sxs-lookup"><span data-stu-id="31cd5-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="31cd5-145">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="31cd5-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

