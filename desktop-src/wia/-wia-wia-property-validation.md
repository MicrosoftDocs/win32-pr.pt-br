---
description: 'Quando um aplicativo executa uma operação IPropertyStorage:: WriteMultiple em qualquer propriedade de aquisição de imagem do Windows (WIA) gravável, o driver WIA executa uma validação no novo valor da propriedade.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validação da propriedade WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164517"
---
# <a name="wia-property-validation"></a><span data-ttu-id="6109e-103">Validação da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-103">WIA Property Validation</span></span>

<span data-ttu-id="6109e-104">Quando um aplicativo executa uma operação [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) em qualquer propriedade de aquisição de imagem do Windows (WIA) gravável, o driver WIA executa uma validação no novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6109e-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="6109e-105">A gravação de uma propriedade pode ter efeitos colaterais que alteram outros valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6109e-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="6109e-106">Cabe ao aplicativo ler todos os valores de propriedade após uma operação de gravação para determinar que todas as propriedades são definidas para os valores que o aplicativo deseja.</span><span class="sxs-lookup"><span data-stu-id="6109e-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="6109e-107">Várias propriedades podem ser gravadas simultaneamente usando a operação [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) .</span><span class="sxs-lookup"><span data-stu-id="6109e-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="6109e-108">Pode haver casos em que algumas atribuições de propriedade entram em conflito.</span><span class="sxs-lookup"><span data-stu-id="6109e-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="6109e-109">Nesses casos, a prioridade usada para resolver conflitos é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="6109e-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="6109e-110">\_tentativa de \_ atual de IPS WIA \_</span><span class="sxs-lookup"><span data-stu-id="6109e-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="6109e-111">\_tipo de \_ dados IPA WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="6109e-112">\_profundidade de IPA WIA \_</span><span class="sxs-lookup"><span data-stu-id="6109e-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="6109e-113">\_XRES IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="6109e-114">\_YRES IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="6109e-115">\_XPos IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="6109e-116">\_YPos IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="6109e-117">\_XEXTENT IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="6109e-118">\_YEXTENT IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="6109e-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="6109e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6109e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6109e-120">**IWiaPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="6109e-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
