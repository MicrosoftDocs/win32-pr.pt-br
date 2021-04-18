---
title: Tipo complexo AttachmentType
description: Define os elementos usados para especificar um anexo enviado com uma mensagem de email.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- tipo complexo AttachmentType Agendador de Tarefas
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759953"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="ff2e9-104">Tipo complexo AttachmentType</span><span class="sxs-lookup"><span data-stu-id="ff2e9-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="ff2e9-105">Define os elementos usados para especificar um anexo enviado com uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ff2e9-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ff2e9-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ff2e9-106">Child elements</span></span>



| <span data-ttu-id="ff2e9-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff2e9-107">Element</span></span>                                                          | <span data-ttu-id="ff2e9-108">Type</span><span class="sxs-lookup"><span data-stu-id="ff2e9-108">Type</span></span>                                                                    | <span data-ttu-id="ff2e9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff2e9-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff2e9-110">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ff2e9-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="ff2e9-111">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="ff2e9-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="ff2e9-112">Especifica o caminho para um arquivo que é enviado como um anexo em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ff2e9-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff2e9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff2e9-113">Requirements</span></span>



| <span data-ttu-id="ff2e9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff2e9-114">Requirement</span></span> | <span data-ttu-id="ff2e9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ff2e9-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff2e9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff2e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff2e9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff2e9-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff2e9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff2e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff2e9-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff2e9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





