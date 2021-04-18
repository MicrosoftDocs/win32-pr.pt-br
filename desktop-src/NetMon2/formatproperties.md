---
description: A função Formatproperties Export formata os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede. Se você quiser exibir dados no painel de detalhes, deverá implementar a função Formatproperties Export em todas as DLLs do analisador.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Função de retorno de chamada formatproperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753428"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="ee41d-104">Função de retorno de chamada formatproperties</span><span class="sxs-lookup"><span data-stu-id="ee41d-104">FormatProperties callback function</span></span>

<span data-ttu-id="ee41d-105">A função **formatproperties** Export formata os dados que são exibidos no painel de detalhes da interface do usuário do monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="ee41d-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="ee41d-106">Se você quiser exibir dados no painel de detalhes, deverá implementar a função **formatproperties** Export em todas as DLLs do analisador.</span><span class="sxs-lookup"><span data-stu-id="ee41d-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee41d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee41d-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="ee41d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee41d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee41d-109">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee41d-110">Identificador para o quadro que está sendo analisado.</span><span class="sxs-lookup"><span data-stu-id="ee41d-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="ee41d-111">*lpFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee41d-112">Ponteiro para o primeiro byte de um quadro.</span><span class="sxs-lookup"><span data-stu-id="ee41d-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="ee41d-113">*lpProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee41d-114">Ponteiro para o início dos dados de protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="ee41d-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="ee41d-115">*nPropertyInsts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee41d-116">Número de estruturas [PROPERTYINST](propertyinst.md) fornecidas por *lpPropInst*.</span><span class="sxs-lookup"><span data-stu-id="ee41d-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="ee41d-117">*lpPropInst* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee41d-118">Ponteiro para uma matriz de estruturas [PROPERTYINST](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="ee41d-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee41d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee41d-119">Return value</span></span>

<span data-ttu-id="ee41d-120">Se a função for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="ee41d-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="ee41d-121">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="ee41d-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee41d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee41d-122">Remarks</span></span>

<span data-ttu-id="ee41d-123">Monitor de Rede chama a função **formatproperties** para exibir dados no painel de detalhes da interface do usuário do monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="ee41d-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="ee41d-124">Normalmente, **formatproperties** é chamado para formatar a linha de Resumo de um protocolo e, em seguida, Formatar todas as instâncias de Propriedade do protocolo dentro de um quadro.</span><span class="sxs-lookup"><span data-stu-id="ee41d-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="ee41d-125">No entanto, Monitor de Rede não garante o número de vezes que ele chama **formatproperties** para um analisador específico.</span><span class="sxs-lookup"><span data-stu-id="ee41d-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="ee41d-126">Durante a implementação da função **formatproperties** , o analisador indiretamente chama a função [FormatPropertyInstance](formatpropertyinstance.md) para usar o formatador genérico que o monitor de rede fornece, ou pode chamar um procedimento formatador personalizado que é definido pelo analisador.</span><span class="sxs-lookup"><span data-stu-id="ee41d-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="ee41d-127">Um dos formatadores deve ser chamado para cada estrutura [PROPERTYINST](propertyinst.md) passada para a DLL do analisador no parâmetro *lpPropInst* .</span><span class="sxs-lookup"><span data-stu-id="ee41d-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="ee41d-128">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="ee41d-128">For Information on</span></span>                                          | <span data-ttu-id="ee41d-129">Consulte</span><span class="sxs-lookup"><span data-stu-id="ee41d-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ee41d-130">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="ee41d-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="ee41d-131">Analisadores</span><span class="sxs-lookup"><span data-stu-id="ee41d-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="ee41d-132">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="ee41d-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="ee41d-133">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="ee41d-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="ee41d-134">Como implementar **formatproperties**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="ee41d-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="ee41d-135">Implementando Formatproperties</span><span class="sxs-lookup"><span data-stu-id="ee41d-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="ee41d-136">Como o formatador genérico formata diferentes tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="ee41d-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="ee41d-137">Saída de formatador genérico</span><span class="sxs-lookup"><span data-stu-id="ee41d-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="ee41d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee41d-138">Requirements</span></span>



| <span data-ttu-id="ee41d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee41d-139">Requirement</span></span> | <span data-ttu-id="ee41d-140">Valor</span><span class="sxs-lookup"><span data-stu-id="ee41d-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee41d-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee41d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ee41d-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ee41d-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee41d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ee41d-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee41d-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ee41d-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee41d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee41d-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee41d-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee41d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee41d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee41d-148">FormatPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="ee41d-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="ee41d-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="ee41d-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="ee41d-150">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="ee41d-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




