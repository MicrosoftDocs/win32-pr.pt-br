---
title: Tipo complexo exectype
description: Define os elementos filho e as informações de sequenciamento do elemento exec (actionproperty).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- tipo complexo de exectype Agendador de Tarefas
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454791"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="df775-104">Tipo complexo exectype</span><span class="sxs-lookup"><span data-stu-id="df775-104">execType Complex Type</span></span>

<span data-ttu-id="df775-105">Define os elementos filho e as informações de sequenciamento do elemento [**exec (actionproperty)**](taskschedulerschema-exec-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="df775-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="df775-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="df775-106">Child elements</span></span>



| <span data-ttu-id="df775-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="df775-107">Element</span></span>                                                                           | <span data-ttu-id="df775-108">Type</span><span class="sxs-lookup"><span data-stu-id="df775-108">Type</span></span>                                                        | <span data-ttu-id="df775-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="df775-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df775-110">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="df775-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="df775-111">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df775-111">**string**</span></span>                                                  | <span data-ttu-id="df775-112">Especifica os argumentos associados à operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="df775-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="df775-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="df775-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="df775-114">**caminhotype**</span><span class="sxs-lookup"><span data-stu-id="df775-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="df775-115">Especifica o arquivo ou documento executável a ser executado.</span><span class="sxs-lookup"><span data-stu-id="df775-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="df775-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="df775-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="df775-117">**caminhotype**</span><span class="sxs-lookup"><span data-stu-id="df775-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="df775-118">Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.</span><span class="sxs-lookup"><span data-stu-id="df775-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="df775-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df775-119">Requirements</span></span>



| <span data-ttu-id="df775-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="df775-120">Requirement</span></span> | <span data-ttu-id="df775-121">Valor</span><span class="sxs-lookup"><span data-stu-id="df775-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df775-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df775-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df775-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df775-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df775-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df775-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df775-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df775-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df775-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="df775-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df775-127">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="df775-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="df775-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="df775-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





