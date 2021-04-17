---
title: Tipo complexo sendEmailType
description: Define o tipo de ação usado para especificar que um email será enviado quando uma tarefa for executada. Esse tipo define todos os elementos usados para modelar a mensagem de email.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Agendador de Tarefas tipo complexo sendEmailType
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769391"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="b583f-105">Tipo complexo sendEmailType</span><span class="sxs-lookup"><span data-stu-id="b583f-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="b583f-106">Define o tipo de ação usado para especificar que um email será enviado quando uma tarefa for executada.</span><span class="sxs-lookup"><span data-stu-id="b583f-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="b583f-107">Esse tipo define todos os elementos usados para modelar a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b583f-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b583f-108">Child elements</span></span>



| <span data-ttu-id="b583f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b583f-109">Element</span></span>                                                                        | <span data-ttu-id="b583f-110">Type</span><span class="sxs-lookup"><span data-stu-id="b583f-110">Type</span></span>                                                                         | <span data-ttu-id="b583f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b583f-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b583f-112">**Anexos**</span><span class="sxs-lookup"><span data-stu-id="b583f-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="b583f-113">**AttachmentType**</span><span class="sxs-lookup"><span data-stu-id="b583f-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="b583f-114">Especifica uma lista de anexos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="b583f-115">**Cco**</span><span class="sxs-lookup"><span data-stu-id="b583f-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="b583f-116">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-116">**string**</span></span>                                                                   | <span data-ttu-id="b583f-117">Especifica os endereços de email usados na linha Cco de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="b583f-118">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="b583f-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="b583f-119">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-119">**string**</span></span>                                                                   | <span data-ttu-id="b583f-120">Especifica o texto no corpo da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="b583f-121">**CC**</span><span class="sxs-lookup"><span data-stu-id="b583f-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="b583f-122">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-122">**string**</span></span>                                                                   | <span data-ttu-id="b583f-123">Especifica os endereços de email usados na linha CC de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="b583f-124">**De**</span><span class="sxs-lookup"><span data-stu-id="b583f-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="b583f-125">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-125">**string**</span></span>                                                                   | <span data-ttu-id="b583f-126">Especifica o endereço de email do remetente.</span><span class="sxs-lookup"><span data-stu-id="b583f-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="b583f-127">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="b583f-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="b583f-128">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="b583f-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="b583f-129">Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="b583f-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="b583f-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="b583f-131">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-131">**string**</span></span>                                                                   | <span data-ttu-id="b583f-132">Especifica os endereços de email que são respondidos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="b583f-133">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="b583f-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="b583f-134">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="b583f-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="b583f-135">Especifica o servidor de email usado para enviar a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="b583f-136">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="b583f-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="b583f-137">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-137">**string**</span></span>                                                                   | <span data-ttu-id="b583f-138">Especifica o assunto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b583f-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="b583f-139">**Para**</span><span class="sxs-lookup"><span data-stu-id="b583f-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="b583f-140">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b583f-140">**string**</span></span>                                                                   | <span data-ttu-id="b583f-141">Especifica os endereços de email para os quais o email será enviado.</span><span class="sxs-lookup"><span data-stu-id="b583f-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="b583f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b583f-142">Requirements</span></span>



| <span data-ttu-id="b583f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b583f-143">Requirement</span></span> | <span data-ttu-id="b583f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b583f-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b583f-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b583f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b583f-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b583f-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b583f-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b583f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b583f-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b583f-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





