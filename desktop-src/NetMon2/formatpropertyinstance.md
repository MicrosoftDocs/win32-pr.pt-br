---
description: Formata os dados da instância de propriedade usando o formatador genérico que o Monitor de Rede fornece.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Função FormatPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790016"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="5a463-103">Função FormatPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="5a463-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="5a463-104">A função **FormatPropertyInstance** formata os dados da instância de propriedade usando o formatador genérico que o monitor de rede fornece.</span><span class="sxs-lookup"><span data-stu-id="5a463-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a463-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a463-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="5a463-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a463-107">*lpPropertyInst* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5a463-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a463-108">Um ponteiro para uma estrutura [PROPERTYINST](propertyinst.md) que contém os dados da instância.</span><span class="sxs-lookup"><span data-stu-id="5a463-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="5a463-109">Na entrada, o formatador genérico usa os dados da instância de um dos membros da União **PROPERTYINST** e converte esses dados em uma cadeia de caracteres formatada predefinida.</span><span class="sxs-lookup"><span data-stu-id="5a463-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="5a463-110">Na saída, o formatador genérico define o membro **szPropertyText** da estrutura **PROPERTYINST** como um ponteiro para a cadeia de caracteres formatada.</span><span class="sxs-lookup"><span data-stu-id="5a463-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a463-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a463-111">Return value</span></span>

<span data-ttu-id="5a463-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="5a463-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5a463-113">Se a função não for bem-sucedida, o valor de retorno será um código de erro de NMerr. h.</span><span class="sxs-lookup"><span data-stu-id="5a463-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a463-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a463-114">Remarks</span></span>

<span data-ttu-id="5a463-115">A DLL do analisador indiretamente chama a função **FormatPropertyInstance** quando o formatador genérico é necessário para formatar dados para exibição no painel de detalhes da interface do usuário do monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="5a463-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="5a463-116">Para chamar **FormatPropertyInstance** , especifique-o no membro **InstanceData** da estrutura [PROPERTYINFO](propertyinfo.md) quando você define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5a463-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="5a463-117">O analisador não reconhece qual função é chamada quando deve formatar uma instância de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="5a463-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="5a463-118">A função pode ser **FormatPropertyInstance** ou uma função de formato personalizada definida pelo analisador.</span><span class="sxs-lookup"><span data-stu-id="5a463-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="5a463-119">O analisador chama qualquer função de formato especificada pelo membro **InstanceData** da estrutura **PROPERTYINFO** para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5a463-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="5a463-120">Para obter mais informações e um exemplo de como implementar [formatproperties](formatproperties.md), consulte [Implementing formatproperties](implementing-formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="5a463-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="5a463-121">Para obter mais informações sobre como o formatador genérico formata diferentes tipos de dados, consulte [saída de formatador genérico](generic-formatter-output.md).</span><span class="sxs-lookup"><span data-stu-id="5a463-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a463-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a463-122">Requirements</span></span>



| <span data-ttu-id="5a463-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a463-123">Requirement</span></span> | <span data-ttu-id="5a463-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5a463-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a463-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a463-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a463-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a463-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5a463-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a463-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a463-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a463-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a463-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5a463-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a463-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a463-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5a463-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a463-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a463-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a463-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a463-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5a463-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a463-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a463-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a463-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a463-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a463-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="5a463-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="5a463-137">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="5a463-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




