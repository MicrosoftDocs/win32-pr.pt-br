---
description: A função AttachPropertyInstance mapeia uma propriedade existente para um local específico nos dados reconhecidos.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Função AttachPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829345"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="050ca-103">Função AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="050ca-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="050ca-104">A função **AttachPropertyInstance** mapeia uma propriedade existente para um local específico nos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="050ca-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="050ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="050ca-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="050ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="050ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="050ca-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-108">Identificador para o quadro que está sendo analisado.</span><span class="sxs-lookup"><span data-stu-id="050ca-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="050ca-109">Use o identificador passado para a DLL do analisador no parâmetro *hFrame* da função [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="050ca-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="050ca-110">*hProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-111">Identificador para uma estrutura de [**PROPERTYINFO**](propertyinfo.md) que define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="050ca-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="050ca-112">Ao implementar a função de exportação de [**registro**](register-parser.md) , você especifica a estrutura **PROPERTYINFO** que define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="050ca-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="050ca-113">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-114">Comprimento dos dados para esta instância da propriedade.</span><span class="sxs-lookup"><span data-stu-id="050ca-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="050ca-115">*lpData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-116">Ponteiro para o local nos dados reconhecidos nos quais o valor da propriedade está localizado.</span><span class="sxs-lookup"><span data-stu-id="050ca-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="050ca-117">Use o ponteiro passado para a DLL do analisador no parâmetro *lpProtocol* da função [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="050ca-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="050ca-118">*HelpID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-119">Identificador (de 0 a 2047) usado para definir a ajuda contextual para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="050ca-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="050ca-120">O número do identificador é relativo ao arquivo de ajuda associado ao [*banco de dados de propriedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="050ca-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="050ca-121">*IndentLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-122">Nível de recuo (de 0 a 15) usado para exibir uma propriedade hierarquicamente.</span><span class="sxs-lookup"><span data-stu-id="050ca-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="050ca-123">Monitor de Rede usa os níveis de 0 a 14 para recuar Propriedades.</span><span class="sxs-lookup"><span data-stu-id="050ca-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="050ca-124">O nível 15 é um valor especial que permite que um analisador anexe uma propriedade oculta que não está visível.</span><span class="sxs-lookup"><span data-stu-id="050ca-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="050ca-125">*IFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="050ca-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050ca-126">Um valor de campo de bits que indica a ordem dos BITs dentro de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="050ca-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="050ca-127">Os analisadores anteriores que definem o *referenciador* como 0 ou 1, agora devem definir o *referenciador* como \_ erro IFLAG.</span><span class="sxs-lookup"><span data-stu-id="050ca-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="050ca-128">Defina esse parâmetro como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="050ca-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="050ca-129">Valor</span><span class="sxs-lookup"><span data-stu-id="050ca-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="050ca-130">Significado</span><span class="sxs-lookup"><span data-stu-id="050ca-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="050ca-131"><dt>**erro de IFLAG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="050ca-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="050ca-132">Os dados no quadro têm um erro.</span><span class="sxs-lookup"><span data-stu-id="050ca-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="050ca-133"><dt>**IFLAG \_ permutado**</dt></span><span class="sxs-lookup"><span data-stu-id="050ca-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="050ca-134">No momento da anexação, o byte de **palavra** é um formato não-Intel.</span><span class="sxs-lookup"><span data-stu-id="050ca-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="050ca-135"><dt>**IFLAG \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="050ca-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="050ca-136">No momento da anexação, a **cadeia de caracteres** é Unicode.</span><span class="sxs-lookup"><span data-stu-id="050ca-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="050ca-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="050ca-137">Return value</span></span>

<span data-ttu-id="050ca-138">Se a função for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="050ca-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="050ca-139">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="050ca-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="050ca-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="050ca-140">Remarks</span></span>

<span data-ttu-id="050ca-141">A função **AttachPropertyInstance** é chamada durante a implementação da função de exportação [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="050ca-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="050ca-142">Quando uma propriedade é anexada aos dados, Monitor de Rede cria uma estrutura [**PROPERTYINST**](propertyinst.md) que define a instância da propriedade anexada.</span><span class="sxs-lookup"><span data-stu-id="050ca-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="050ca-143">Durante a implementação de [**attachproperties**](attachproperties.md), chame **AttachPropertyInstance** para usar os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="050ca-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="050ca-144">Você também pode chamar a função [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para modificar os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="050ca-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="050ca-145">No entanto, é recomendável que você use os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="050ca-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="050ca-146">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="050ca-146">For Information on</span></span>                                        | <span data-ttu-id="050ca-147">Consulte</span><span class="sxs-lookup"><span data-stu-id="050ca-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="050ca-148">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="050ca-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="050ca-149">**Analisadores**</span><span class="sxs-lookup"><span data-stu-id="050ca-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="050ca-150">Como chamar **AttachPropertyInstance**.</span><span class="sxs-lookup"><span data-stu-id="050ca-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="050ca-151">Implementando Anexaproperties</span><span class="sxs-lookup"><span data-stu-id="050ca-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="050ca-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="050ca-152">Requirements</span></span>



| <span data-ttu-id="050ca-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="050ca-153">Requirement</span></span> | <span data-ttu-id="050ca-154">Valor</span><span class="sxs-lookup"><span data-stu-id="050ca-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="050ca-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="050ca-155">Minimum supported client</span></span><br/> | <span data-ttu-id="050ca-156">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="050ca-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="050ca-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="050ca-157">Minimum supported server</span></span><br/> | <span data-ttu-id="050ca-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="050ca-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="050ca-159">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="050ca-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="050ca-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="050ca-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="050ca-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="050ca-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="050ca-162"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="050ca-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="050ca-163">DLL</span><span class="sxs-lookup"><span data-stu-id="050ca-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="050ca-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="050ca-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050ca-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="050ca-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050ca-166">**Anexarproperties**</span><span class="sxs-lookup"><span data-stu-id="050ca-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="050ca-167">**AttachPropertyInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="050ca-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="050ca-168">**PROPERTYINST**</span><span class="sxs-lookup"><span data-stu-id="050ca-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




