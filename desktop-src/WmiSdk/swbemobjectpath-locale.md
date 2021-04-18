---
description: A propriedade locale do objeto SWbemObjectPath contém a localidade do caminho do objeto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. Locale (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781610"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="0ddd0-103">Propriedade SWbemObjectPath. Locale</span><span class="sxs-lookup"><span data-stu-id="0ddd0-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="0ddd0-104">A propriedade **locale** do objeto [**SWbemObjectPath**](swbemobjectpath.md) contém a localidade do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="0ddd0-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="0ddd0-105">Quando a propriedade **SWbemObjectPath. Locale** faz parte de um objeto [**SWbemObjectPath**](swbemobjectpath.md) autônomo, ela é de leitura/gravação e pode ser usada para definir o componente de localidade do moniker.</span><span class="sxs-lookup"><span data-stu-id="0ddd0-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="0ddd0-106">Quando a propriedade **SWbemObjectPath. Locale** é acessada como parte de uma propriedade [**\_ SWbemObject. Path**](swbemobject-path-.md) , ela é somente leitura e relata o valor da localidade usada na associação ao namespace do qual o objeto foi obtido.</span><span class="sxs-lookup"><span data-stu-id="0ddd0-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="0ddd0-107">Para identificadores de localidade da Microsoft, o formato da cadeia de caracteres é "MS \_ xxxx", onde xxxx é uma cadeia de caracteres no formato hexadecimal que indica o LCID.</span><span class="sxs-lookup"><span data-stu-id="0ddd0-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="0ddd0-108">Por exemplo, o identificador de localidade inglês americano é "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="0ddd0-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="0ddd0-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0ddd0-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0ddd0-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0ddd0-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddd0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ddd0-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="0ddd0-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0ddd0-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddd0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ddd0-113">Requirements</span></span>



| <span data-ttu-id="0ddd0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ddd0-114">Requirement</span></span> | <span data-ttu-id="0ddd0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0ddd0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddd0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ddd0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddd0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ddd0-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ddd0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ddd0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddd0-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ddd0-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ddd0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ddd0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddd0-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddd0-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ddd0-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0ddd0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ddd0-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0ddd0-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0ddd0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0ddd0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ddd0-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ddd0-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0ddd0-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="0ddd0-126">CLSID</span></span><br/>                    | <span data-ttu-id="0ddd0-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="0ddd0-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="0ddd0-128">IID</span><span class="sxs-lookup"><span data-stu-id="0ddd0-128">IID</span></span><br/>                      | <span data-ttu-id="0ddd0-129">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="0ddd0-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




