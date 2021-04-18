---
description: A função AttachPropertyInstanceEx mapeia uma propriedade existente para um local específico nos dados reconhecidos e modifica o valor dos dados da propriedade.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Função AttachPropertyInstanceEx (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758594"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="7c656-103">Função AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="7c656-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="7c656-104">A função **AttachPropertyInstanceEx** mapeia uma propriedade existente para um local específico nos dados reconhecidos e modifica o valor dos dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c656-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c656-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7c656-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c656-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-108">Identificador para o quadro que está sendo analisado.</span><span class="sxs-lookup"><span data-stu-id="7c656-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="7c656-109">Use o identificador passado para a DLL do analisador no parâmetro *hFrame* da função [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="7c656-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-110">*hProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-111">Identificador para uma estrutura de [**PROPERTYINFO**](propertyinfo.md) que define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="7c656-112">Ao implementar a função de exportação de [**registro**](register-parser.md) , você especifica a estrutura **PROPERTYINFO** que define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-113">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-114">Comprimento dos dados para esta instância da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-115">*lpData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-116">Ponteiro para o local nos dados reconhecidos nos quais o valor da propriedade está localizado.</span><span class="sxs-lookup"><span data-stu-id="7c656-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="7c656-117">Use o ponteiro passado para a DLL do analisador no parâmetro *lpProtocol* da função [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="7c656-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-118">*LengthEx* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-119">Comprimento do tamanho dos dados estendidos em bytes.</span><span class="sxs-lookup"><span data-stu-id="7c656-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-120">*lpDataEx* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-121">Ponteiro para os dados estendidos, que normalmente é uma variável de pilha que contém os dados de extensão.</span><span class="sxs-lookup"><span data-stu-id="7c656-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-122">*HelpID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-123">Identificador (de 0 a 2047) usado para definir a ajuda contextual para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="7c656-124">O número da *ajuda* é relativo ao arquivo de ajuda associado ao banco de [*dados de propriedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7c656-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c656-125">*IndentLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-126">Nível de recuo (de 0 a 15) usado para exibir uma propriedade hierarquicamente.</span><span class="sxs-lookup"><span data-stu-id="7c656-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="7c656-127">Monitor de Rede usa os níveis de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="7c656-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="7c656-128">O nível 15 é um valor especial que permite que o analisador anexe uma propriedade oculta que não está visível.</span><span class="sxs-lookup"><span data-stu-id="7c656-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="7c656-129">*IFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c656-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c656-130">Um valor de campo de bits que indica a ordem dos BITs dentro de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="7c656-131">Os analisadores anteriores que definem o *referenciador* como 0 ou 1, agora devem definir o *referenciador* como \_ erro IFLAG.</span><span class="sxs-lookup"><span data-stu-id="7c656-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="7c656-132">Defina esse parâmetro como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7c656-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="7c656-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7c656-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="7c656-134">Significado</span><span class="sxs-lookup"><span data-stu-id="7c656-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="7c656-135"><dt>**erro de IFLAG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c656-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="7c656-136">Os dados no quadro têm um erro.</span><span class="sxs-lookup"><span data-stu-id="7c656-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="7c656-137"><dt>**IFLAG \_ permutado**</dt></span><span class="sxs-lookup"><span data-stu-id="7c656-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="7c656-138">No momento da anexação, o byte de **palavra** é um formato não-Intel.</span><span class="sxs-lookup"><span data-stu-id="7c656-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="7c656-139"><dt>**IFLAG \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="7c656-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="7c656-140">No momento da anexação, a **cadeia de caracteres** é Unicode.</span><span class="sxs-lookup"><span data-stu-id="7c656-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c656-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c656-141">Return value</span></span>

<span data-ttu-id="7c656-142">Se a função for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="7c656-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="7c656-143">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="7c656-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c656-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c656-144">Remarks</span></span>

<span data-ttu-id="7c656-145">A função **AttachPropertyInstanceEx** é chamada durante a implementação da função de exportação [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="7c656-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="7c656-146">Quando uma propriedade é anexada aos dados usando AttachPropertyInstanceEx, Monitor de Rede cria uma estrutura [**PROPERTYINST**](propertyinst.md) que define a instância da propriedade anexada e uma estrutura [**PROPERTYINSTEX**](propertyinstex.md) que define os dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="7c656-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="7c656-147">Se **AttachPropertyInstanceEx** for chamado e nenhum dado estendido for fornecido, o parâmetro *lpDataEx* será **nulo** ou o parâmetro *LengthEx* será 0, a chamada **AttachPropertyInstanceEx** será funcionalmente equivalente a uma chamada [**AttachPropertyInstance**](attachpropertyinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="7c656-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="7c656-148">Durante a implementação de [**attachproperties**](attachproperties.md), chame [**AttachPropertyInstance**](attachpropertyinstance.md) para usar os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="7c656-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="7c656-149">Você também pode chamar a função **AttachPropertyInstanceEx** para modificar os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c656-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="7c656-150">No entanto, é recomendável que você use os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="7c656-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c656-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c656-151">Requirements</span></span>



| <span data-ttu-id="7c656-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c656-152">Requirement</span></span> | <span data-ttu-id="7c656-153">Valor</span><span class="sxs-lookup"><span data-stu-id="7c656-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c656-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c656-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7c656-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c656-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7c656-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c656-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7c656-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c656-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7c656-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c656-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c656-159"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c656-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7c656-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c656-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c656-161"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c656-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c656-162">DLL</span><span class="sxs-lookup"><span data-stu-id="7c656-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c656-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c656-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




