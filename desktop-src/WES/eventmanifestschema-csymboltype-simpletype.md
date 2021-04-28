---
title: Tipo simples de CSymbolType (log de eventos do Windows)
description: Tipo simples de CSymbolType (log de eventos do Windows) – define um nome de símbolo C/C++ válido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Log de eventos de tipo simples CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090614"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="0edd3-104">Tipo simples de CSymbolType (log de eventos do Windows)</span><span class="sxs-lookup"><span data-stu-id="0edd3-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="0edd3-105">Define um nome de símbolo do C/C++ válido.</span><span class="sxs-lookup"><span data-stu-id="0edd3-105">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="0edd3-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="0edd3-106">Patterns</span></span>

<span data-ttu-id="0edd3-107">O tipo simples **CSymbolType** é um **xs: String** que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="0edd3-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="0edd3-108">O nome do símbolo pode ser vazio ou conter caracteres alfanuméricos e sublinhados.</span><span class="sxs-lookup"><span data-stu-id="0edd3-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="0edd3-109">Se o nome estiver vazio, o compilador de mensagem irá gerar o nome do símbolo.</span><span class="sxs-lookup"><span data-stu-id="0edd3-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="0edd3-110">Se você especificar um nome, o nome deverá começar com um sublinhado ( \_ ) ou um caractere alfabético.</span><span class="sxs-lookup"><span data-stu-id="0edd3-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="0edd3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0edd3-111">Remarks</span></span>

<span data-ttu-id="0edd3-112">Se o nome do símbolo estiver vazio, o compilador de mensagem usará o atributo **Name** do elemento que você está definindo para gerar o nome do símbolo.</span><span class="sxs-lookup"><span data-stu-id="0edd3-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="0edd3-113">O compilador substitui os caracteres não alfanuméricos e os dígitos à esquerda por sublinhados.</span><span class="sxs-lookup"><span data-stu-id="0edd3-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="0edd3-114">Por exemplo, se o atributo de **nome** do canal for Microsoft-Windows-SampleProvider/Operational, o compilador usará o Microsoft \_ Windows \_ SampleProvider \_ operacional como o nome do símbolo.</span><span class="sxs-lookup"><span data-stu-id="0edd3-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="0edd3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edd3-115">Requirements</span></span>



| <span data-ttu-id="0edd3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edd3-116">Requirement</span></span> | <span data-ttu-id="0edd3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0edd3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0edd3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edd3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0edd3-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0edd3-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0edd3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edd3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0edd3-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0edd3-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





