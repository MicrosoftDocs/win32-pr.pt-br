---
description: Contém informações que identificam o adaptador.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Estrutura de D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129965"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="51b66-103">\_Estrutura D3DADAPTER IDENTIFIER9</span><span class="sxs-lookup"><span data-stu-id="51b66-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="51b66-104">Contém informações que identificam o adaptador.</span><span class="sxs-lookup"><span data-stu-id="51b66-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51b66-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="51b66-106">Membros</span><span class="sxs-lookup"><span data-stu-id="51b66-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51b66-107">**Driver**</span><span class="sxs-lookup"><span data-stu-id="51b66-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-108">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="51b66-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-109">Usado para apresentação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="51b66-109">Used for presentation to the user.</span></span> <span data-ttu-id="51b66-110">Isso não deve ser usado para identificar drivers específicos, pois muitas cadeias de caracteres diferentes podem ser associadas ao mesmo dispositivo e driver de fornecedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="51b66-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51b66-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-112">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="51b66-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-113">Usado para apresentação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="51b66-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="51b66-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-115">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="51b66-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-116">Nome do dispositivo para GDI.</span><span class="sxs-lookup"><span data-stu-id="51b66-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="51b66-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-118">Tipo: **[ **\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="51b66-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-119">Identifique a versão do driver do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="51b66-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="51b66-120">É legal fazer menos de e maior que comparações no valor inteiro com sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="51b66-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="51b66-121">No entanto, tome cuidado se você usar esse elemento para identificar drivers problemáticos.</span><span class="sxs-lookup"><span data-stu-id="51b66-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="51b66-122">Em vez disso, você deve usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="51b66-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="51b66-123">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="51b66-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="51b66-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-126">Identifique a versão do driver do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="51b66-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="51b66-127">É legal fazer < e > comparações no valor inteiro assinado de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="51b66-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="51b66-128">No entanto, tome cuidado se você usar esse elemento para identificar drivers problemáticos.</span><span class="sxs-lookup"><span data-stu-id="51b66-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="51b66-129">Em vez disso, você deve usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="51b66-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="51b66-130">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="51b66-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="51b66-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-133">Identifique a versão do driver do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="51b66-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="51b66-134">É legal fazer < e > comparações no valor inteiro assinado de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="51b66-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="51b66-135">No entanto, tome cuidado se você usar esse elemento para identificar drivers problemáticos.</span><span class="sxs-lookup"><span data-stu-id="51b66-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="51b66-136">Em vez disso, você deve usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="51b66-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="51b66-137">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="51b66-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="51b66-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-140">Pode ser usado para ajudar a identificar um determinado conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="51b66-141">Consulte este membro para identificar o fabricante.</span><span class="sxs-lookup"><span data-stu-id="51b66-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="51b66-142">O valor pode ser zero se for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="51b66-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="51b66-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-145">Pode ser usado para ajudar a identificar um determinado conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="51b66-146">Consulte este membro para identificar o tipo de conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="51b66-147">O valor pode ser zero se for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="51b66-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="51b66-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-150">Pode ser usado para ajudar a identificar um determinado conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="51b66-151">Consulte este membro para identificar o subsistema, normalmente o quadro específico.</span><span class="sxs-lookup"><span data-stu-id="51b66-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="51b66-152">O valor pode ser zero se for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="51b66-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-153">**Revisão**</span><span class="sxs-lookup"><span data-stu-id="51b66-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-155">Pode ser usado para ajudar a identificar um determinado conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="51b66-156">Consulte este membro para identificar o nível de revisão do conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="51b66-157">O valor pode ser zero se for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="51b66-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="51b66-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-159">Tipo: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-160">Pode ser consultado para verificar as alterações no driver e no conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="51b66-161">Esse GUID é um identificador exclusivo para o par de drivers e conjuntos de chips.</span><span class="sxs-lookup"><span data-stu-id="51b66-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="51b66-162">Consulte este membro para controlar as alterações no driver e no conjunto de chips para gerar um novo perfil para o subsistema de gráficos.</span><span class="sxs-lookup"><span data-stu-id="51b66-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="51b66-163">O DeviceIdentifier também pode ser usado para identificar drivers problemáticos específicos.</span><span class="sxs-lookup"><span data-stu-id="51b66-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="51b66-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="51b66-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="51b66-165">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b66-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51b66-166">Usado para determinar o nível de validação do WHQL (Windows Hardware Quality Labs) para este driver e par de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="51b66-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="51b66-167">O DWORD é uma estrutura de data empacotada que define a data da versão do teste WHQL mais recente passado pelo driver.</span><span class="sxs-lookup"><span data-stu-id="51b66-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="51b66-168">É legal executar < e > operações nesse valor.</span><span class="sxs-lookup"><span data-stu-id="51b66-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="51b66-169">O seguinte ilustra o formato de data.</span><span class="sxs-lookup"><span data-stu-id="51b66-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="51b66-170">Bits</span><span class="sxs-lookup"><span data-stu-id="51b66-170">Bits</span></span>  |  <span data-ttu-id="51b66-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="51b66-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="51b66-172">31-16</span><span class="sxs-lookup"><span data-stu-id="51b66-172">31-16</span></span> | <span data-ttu-id="51b66-173">O ano, um número decimal de 1999 para cima.</span><span class="sxs-lookup"><span data-stu-id="51b66-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="51b66-174">15-8</span><span class="sxs-lookup"><span data-stu-id="51b66-174">15-8</span></span>  | <span data-ttu-id="51b66-175">O mês, um número decimal de 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="51b66-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="51b66-176">7-0</span><span class="sxs-lookup"><span data-stu-id="51b66-176">7-0</span></span>   | <span data-ttu-id="51b66-177">O dia, um número decimal de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="51b66-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="51b66-178">Os valores a seguir também são usados.</span><span class="sxs-lookup"><span data-stu-id="51b66-178">The following values are also used.</span></span>



| <span data-ttu-id="51b66-179">Valor</span><span class="sxs-lookup"><span data-stu-id="51b66-179">Value</span></span>    |  <span data-ttu-id="51b66-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="51b66-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="51b66-181">0</span><span class="sxs-lookup"><span data-stu-id="51b66-181">0</span></span>   | <span data-ttu-id="51b66-182">Não certificado.</span><span class="sxs-lookup"><span data-stu-id="51b66-182">Not certified.</span></span>                                        |
| <span data-ttu-id="51b66-183">1</span><span class="sxs-lookup"><span data-stu-id="51b66-183">1</span></span>   | <span data-ttu-id="51b66-184">O WHQL foi validado, mas nenhuma informação de data está disponível.</span><span class="sxs-lookup"><span data-stu-id="51b66-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="51b66-185">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="51b66-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="51b66-186">Para o Direct3D9Ex em execução no Windows Vista, no Windows Server 2008, no Windows 7 e no Windows Server 2008 R2 (ou mais no sistema operacional atual), [**IDirect3D9:: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) retorna 1 para o nível de WHQL sem verificar o status do driver.</span><span class="sxs-lookup"><span data-stu-id="51b66-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51b66-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="51b66-187">Remarks</span></span>

<span data-ttu-id="51b66-188">O exemplo de pseudocódigo a seguir ilustra o formato de versão codificado nos membros DriverVersion, DriverVersionLowPart e DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="51b66-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="51b66-189">Consulte o SDK da plataforma para obter mais informações sobre a macro HIWORD, a macro LOWORD e a \_ estrutura de inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="51b66-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="51b66-190">\_ \_ A cadeia de caracteres máxima do identificador de dispositivo \_ é uma constante com a definição a seguir.</span><span class="sxs-lookup"><span data-stu-id="51b66-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="51b66-191">Os membros VendorID, DeviceID, SubSysId e Revision podem ser usados em conjunto para identificar conjuntos de chips específicos.</span><span class="sxs-lookup"><span data-stu-id="51b66-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="51b66-192">No entanto, use esses membros com cuidado.</span><span class="sxs-lookup"><span data-stu-id="51b66-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b66-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51b66-193">Requirements</span></span>



| <span data-ttu-id="51b66-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="51b66-194">Requirement</span></span> | <span data-ttu-id="51b66-195">Valor</span><span class="sxs-lookup"><span data-stu-id="51b66-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51b66-196">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51b66-196">Header</span></span><br/> | <dl> <span data-ttu-id="51b66-197"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b66-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b66-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="51b66-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b66-199">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="51b66-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
