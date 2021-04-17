---
description: A propriedade SummaryInformation do objeto Database retorna um objeto SummaryInfo que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de resumo.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Propriedade Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748596"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="92e6f-103">Propriedade Database. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="92e6f-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="92e6f-104">A propriedade **SummaryInformation** do objeto [**Database**](database-object.md) retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao [fluxo de informações de resumo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="92e6f-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="92e6f-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="92e6f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e6f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92e6f-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="92e6f-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="92e6f-107">Property value</span></span>

<span data-ttu-id="92e6f-108">O número máximo de propriedades a serem adicionadas ou modificadas.</span><span class="sxs-lookup"><span data-stu-id="92e6f-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="92e6f-109">Esse parâmetro é necessário e usado para alocar memória de trabalho suficiente durante a geração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="92e6f-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="92e6f-110">Não é necessário armazenar esse número de propriedades.</span><span class="sxs-lookup"><span data-stu-id="92e6f-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="92e6f-111">Um valor de zero deve ser usado se o banco de dados for aberto como somente leitura para impedir que o fluxo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="92e6f-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="92e6f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="92e6f-112">Remarks</span></span>

<span data-ttu-id="92e6f-113">Se um valor de *maxProperties* maior que 0 for usado para abrir um fluxo de informações de resumo existente, o método [**Persist**](summaryinfo-persist.md) deverá ser chamado antes de fechar o objeto.</span><span class="sxs-lookup"><span data-stu-id="92e6f-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="92e6f-114">A falha ao fazer isso perderá as informações de fluxo existentes.</span><span class="sxs-lookup"><span data-stu-id="92e6f-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="92e6f-115">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="92e6f-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e6f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e6f-116">Requirements</span></span>



| <span data-ttu-id="92e6f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e6f-117">Requirement</span></span> | <span data-ttu-id="92e6f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="92e6f-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e6f-119">Versão</span><span class="sxs-lookup"><span data-stu-id="92e6f-119">Version</span></span><br/> | <span data-ttu-id="92e6f-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92e6f-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92e6f-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92e6f-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92e6f-122">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="92e6f-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="92e6f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="92e6f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="92e6f-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92e6f-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="92e6f-125">IID</span><span class="sxs-lookup"><span data-stu-id="92e6f-125">IID</span></span><br/>     | <span data-ttu-id="92e6f-126">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="92e6f-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




