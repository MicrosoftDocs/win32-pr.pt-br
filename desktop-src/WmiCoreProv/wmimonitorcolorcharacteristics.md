---
description: Representa as características de cor da CIE (Comissão Internacional de iluminação) de um monitor de computador.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Classe WmiMonitorColorCharacteristics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296950"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="8bcd2-103">Classe WmiMonitorColorCharacteristics</span><span class="sxs-lookup"><span data-stu-id="8bcd2-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="8bcd2-104">A classe **WmiMonitorColorCharacteristics** representa as características de cor da CIE (Comissão Internacional sobre iluminação) de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="8bcd2-105">Os dados correspondem aos dados no bloco de características de cores da estrutura E-EDID (dados de identificação de exibição estendida) avançada da VESA (Video Electronics Standard Association).</span><span class="sxs-lookup"><span data-stu-id="8bcd2-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcd2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bcd2-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="8bcd2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8bcd2-107">Members</span></span>

<span data-ttu-id="8bcd2-108">A classe **WmiMonitorColorCharacteristics** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8bcd2-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="8bcd2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bcd2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bcd2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bcd2-110">Properties</span></span>

<span data-ttu-id="8bcd2-111">A classe **WmiMonitorColorCharacteristics** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bcd2-112">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcd2-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bcd2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bcd2-115">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="8bcd2-116">**Azul**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcd2-117">Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bcd2-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bcd2-119">Coordenadas de CIE para Blue, representadas por uma instância da classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="8bcd2-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8bcd2-120">**Defaultwhite**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcd2-121">Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bcd2-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bcd2-123">Coordenadas de CIE branco padrão.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8bcd2-124">**Verde**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcd2-125">Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bcd2-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bcd2-127">Coordenadas de CIE para verde, representadas por uma instância da classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="8bcd2-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8bcd2-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcd2-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bcd2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-131">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8bcd2-132">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="8bcd2-133">**Vermelho**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcd2-134">Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8bcd2-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bcd2-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bcd2-136">Coordenadas de CIE para vermelho, representadas por uma instância da classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="8bcd2-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bcd2-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bcd2-137">Remarks</span></span>

<span data-ttu-id="8bcd2-138">Os valores de desvio e de ponto branco são expressos como números fracionários usando um formato de codificação.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="8bcd2-139">Esse formato é preciso para o lugar de milhares, que tem 10 bits de comprimento.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="8bcd2-140">O bit mais significativo (MSB) representa 2 ^-1 e o bit menos significativo (LSB) representa dois coeficientes de ^-10, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="8bcd2-141">A precisão dos valores armazenados na estrutura E-EDID v1. x deve ser precisa de +/-0, 5 do valor real.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bcd2-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bcd2-142">Requirements</span></span>



| <span data-ttu-id="8bcd2-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcd2-143">Requirement</span></span> | <span data-ttu-id="8bcd2-144">Valor</span><span class="sxs-lookup"><span data-stu-id="8bcd2-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcd2-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bcd2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcd2-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bcd2-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8bcd2-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bcd2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcd2-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bcd2-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8bcd2-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bcd2-149">Namespace</span></span><br/>                | <span data-ttu-id="8bcd2-150">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="8bcd2-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="8bcd2-151">MOF</span><span class="sxs-lookup"><span data-stu-id="8bcd2-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bcd2-152"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bcd2-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bcd2-153">DLL</span><span class="sxs-lookup"><span data-stu-id="8bcd2-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bcd2-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bcd2-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bcd2-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bcd2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcd2-156">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




