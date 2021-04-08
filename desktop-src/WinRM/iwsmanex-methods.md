---
title: Métodos IWSManEx
description: A interface IWSManEx expõe os métodos a seguir.
ms.assetid: 609F5D75-879A-4681-B746-8C7A8757F062
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7279d15d98b3e534e57a83813cd9cbe75a09fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004800"
---
# <a name="iwsmanex-methods"></a><span data-ttu-id="6512b-103">Métodos IWSManEx</span><span class="sxs-lookup"><span data-stu-id="6512b-103">IWSManEx Methods</span></span>

<span data-ttu-id="6512b-104">A interface [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="6512b-104">The [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6512b-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6512b-105">In this section</span></span>

-   [<span data-ttu-id="6512b-106">**Método CreateResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="6512b-106">**CreateResourceLocator Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
-   [<span data-ttu-id="6512b-107">**Método EnumerationFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="6512b-107">**EnumerationFlagHierarchyDeep Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)
-   [<span data-ttu-id="6512b-108">**Método EnumerationFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="6512b-108">**EnumerationFlagHierarchyDeepBasePropsOnly Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)
-   [<span data-ttu-id="6512b-109">**Método EnumerationFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="6512b-109">**EnumerationFlagHierarchyShallow Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)
-   [<span data-ttu-id="6512b-110">**Método EnumerationFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="6512b-110">**EnumerationFlagNonXmlText Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)
-   [<span data-ttu-id="6512b-111">**Método EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="6512b-111">**EnumerationFlagReturnEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)
-   [<span data-ttu-id="6512b-112">**Método EnumerationFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="6512b-112">**EnumerationFlagReturnObject Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)
-   [<span data-ttu-id="6512b-113">**Método EnumerationFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="6512b-113">**EnumerationFlagReturnObjectAndEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)
-   [<span data-ttu-id="6512b-114">**Método GetErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="6512b-114">**GetErrorMessage Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)
-   [<span data-ttu-id="6512b-115">**Método SessionFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="6512b-115">**SessionFlagCredUsernamePassword Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)
-   [<span data-ttu-id="6512b-116">**Método SessionFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="6512b-116">**SessionFlagEnableSPNServerPort Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)
-   [<span data-ttu-id="6512b-117">**Método SessionFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="6512b-117">**SessionFlagNoEncryption Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)
-   [<span data-ttu-id="6512b-118">**Método SessionFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="6512b-118">**SessionFlagSkipCACheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)
-   [<span data-ttu-id="6512b-119">**Método SessionFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="6512b-119">**SessionFlagSkipCNCheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)
-   [<span data-ttu-id="6512b-120">**Método SessionFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="6512b-120">**SessionFlagUseBasic Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)
-   [<span data-ttu-id="6512b-121">**Método SessionFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="6512b-121">**SessionFlagUseDigest Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)
-   [<span data-ttu-id="6512b-122">**Método SessionFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="6512b-122">**SessionFlagUseKerberos Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)
-   [<span data-ttu-id="6512b-123">**Método SessionFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="6512b-123">**SessionFlagUseNegotiate Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)
-   [<span data-ttu-id="6512b-124">**Método SessionFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="6512b-124">**SessionFlagUseNoAuthentication Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)
-   [<span data-ttu-id="6512b-125">**Método SessionFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="6512b-125">**SessionFlagUTF8 Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)

 

 




