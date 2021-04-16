---
description: A propriedade QualifierDescription somente leitura retorna uma cadeia de texto que descreve o componente qualificado.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Propriedade Installer. QualifierDescription
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752250"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="3207f-103">Propriedade Installer. QualifierDescription</span><span class="sxs-lookup"><span data-stu-id="3207f-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="3207f-104">A propriedade **QualifierDescription** somente leitura retorna uma cadeia de texto que descreve o componente qualificado.</span><span class="sxs-lookup"><span data-stu-id="3207f-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="3207f-105">Essa cadeia de caracteres localizável é criada na coluna AppData da [tabela PublishComponent](publishcomponent-table.md) e pode ser exibida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3207f-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="3207f-106">O qualificador distingue várias formas do mesmo componente, como um componente que é implementado em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="3207f-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="3207f-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3207f-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3207f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3207f-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="3207f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3207f-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="3207f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3207f-110">Requirements</span></span>



| <span data-ttu-id="3207f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3207f-111">Requirement</span></span> | <span data-ttu-id="3207f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3207f-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3207f-113">Versão</span><span class="sxs-lookup"><span data-stu-id="3207f-113">Version</span></span><br/> | <span data-ttu-id="3207f-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3207f-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3207f-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3207f-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3207f-116">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3207f-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3207f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3207f-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="3207f-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3207f-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3207f-119">IID</span><span class="sxs-lookup"><span data-stu-id="3207f-119">IID</span></span><br/>     | <span data-ttu-id="3207f-120">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3207f-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3207f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3207f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3207f-122">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="3207f-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="3207f-123">Componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="3207f-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




