---
description: Define o tipo que define valores válidos para o atributo Type do leitor de diário de elementos de conteúdo \[ \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo simples de ContentTypetype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011174"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="44f76-103">Tipo simples de ContentTypetype</span><span class="sxs-lookup"><span data-stu-id="44f76-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="44f76-104">Define o tipo que define valores válidos para o atributo *Type* do [leitor \[ \] de diário de elementos de conteúdo](content-element--journal-reader.md).</span><span class="sxs-lookup"><span data-stu-id="44f76-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="44f76-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="44f76-105">Patterns</span></span>

<span data-ttu-id="44f76-106">O tipo simples **contenttypetype** é uma cadeia de caracteres que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="44f76-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="44f76-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f76-107">Remarks</span></span>

<span data-ttu-id="44f76-108">Os valores válidos são "normal" e "Inert".</span><span class="sxs-lookup"><span data-stu-id="44f76-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="44f76-109">Se o tipo for "Inert", o conteúdo contido será uma página de diário que é o "plano de fundo" somente leitura/não editável para o documento.</span><span class="sxs-lookup"><span data-stu-id="44f76-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="44f76-110">Isso ocorre quando um documento é criado usando o driver de impressora do gravador de notas do diário.</span><span class="sxs-lookup"><span data-stu-id="44f76-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f76-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44f76-111">Requirements</span></span>



| <span data-ttu-id="44f76-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="44f76-112">Requirement</span></span> | <span data-ttu-id="44f76-113">Valor</span><span class="sxs-lookup"><span data-stu-id="44f76-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="44f76-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44f76-114">Minimum supported client</span></span><br/> | <span data-ttu-id="44f76-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="44f76-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44f76-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44f76-116">Minimum supported server</span></span><br/> | <span data-ttu-id="44f76-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="44f76-117">None supported</span></span><br/>                                     |



 

 




