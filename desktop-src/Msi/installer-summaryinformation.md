---
description: A propriedade SummaryInformation do objeto do instalador retorna um objeto SummaryInfo que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de Resumo de um pacote ou transformação.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Propriedade Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751647"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="39692-103">Propriedade Installer. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="39692-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="39692-104">A propriedade **SummaryInformation** do objeto do [**instalador**](installer-object.md) retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de Resumo de um pacote ou transformação.</span><span class="sxs-lookup"><span data-stu-id="39692-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="39692-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="39692-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39692-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39692-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="39692-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="39692-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="39692-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="39692-108">Remarks</span></span>

<span data-ttu-id="39692-109">Se um valor de *maxProperties* maior que 0 for usado para abrir um fluxo de informações de resumo existente, o método [**Persist**](summaryinfo-persist.md) deverá ser chamado antes de fechar o objeto.</span><span class="sxs-lookup"><span data-stu-id="39692-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="39692-110">A falha de fazer isso perde as informações de fluxo existentes.</span><span class="sxs-lookup"><span data-stu-id="39692-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39692-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39692-111">Requirements</span></span>



| <span data-ttu-id="39692-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="39692-112">Requirement</span></span> | <span data-ttu-id="39692-113">Valor</span><span class="sxs-lookup"><span data-stu-id="39692-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39692-114">Versão</span><span class="sxs-lookup"><span data-stu-id="39692-114">Version</span></span><br/> | <span data-ttu-id="39692-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="39692-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="39692-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="39692-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="39692-117">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="39692-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="39692-118">DLL</span><span class="sxs-lookup"><span data-stu-id="39692-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="39692-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39692-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="39692-120">IID</span><span class="sxs-lookup"><span data-stu-id="39692-120">IID</span></span><br/>     | <span data-ttu-id="39692-121">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="39692-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




