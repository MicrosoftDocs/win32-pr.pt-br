---
description: Saiba mais sobre as classes WMI C++ que fazem parte do WMI Provider Framework e agora são consideradas no estado final.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Provider Framework Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120441"
---
# <a name="provider-framework-classes"></a><span data-ttu-id="9d1f3-103">Provider Framework Classes</span><span class="sxs-lookup"><span data-stu-id="9d1f3-103">Provider Framework Classes</span></span>

<span data-ttu-id="9d1f3-104">\[As classes WMI C++ que fazem parte do WMI Provider Framework agora são consideradas no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-104">\[WMI C++ classes that are part of the WMI Provider Framework are are now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9d1f3-105">As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="9d1f3-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9d1f3-106">A estrutura do provedor implementa as classes a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-106">The provider framework implements the following classes.</span></span>



| <span data-ttu-id="9d1f3-107">Classe Framework</span><span class="sxs-lookup"><span data-stu-id="9d1f3-107">Framework class</span></span>                                | <span data-ttu-id="9d1f3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d1f3-108">Description</span></span>                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d1f3-109">**CFrameworkQuery**</span><span class="sxs-lookup"><span data-stu-id="9d1f3-109">**CFrameworkQuery**</span></span>](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | <span data-ttu-id="9d1f3-110">Contém métodos para processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-110">Contains methods for query processing.</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="9d1f3-111">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="9d1f3-111">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)                 | <span data-ttu-id="9d1f3-112">Contém métodos para definir e recuperar propriedades e é um encapsulamento da interface [**IWbemClassObject.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)</span><span class="sxs-lookup"><span data-stu-id="9d1f3-112">Contains methods to set and retrieve properties and is an encapsulation of the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span> <span data-ttu-id="9d1f3-113">O implementador não deve ter que acessar os **métodos IWbemClassObject** diretamente.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-113">Implementer should not have to access **IWbemClassObject** methods directly.</span></span> |
| [<span data-ttu-id="9d1f3-114">**CThreadBase**</span><span class="sxs-lookup"><span data-stu-id="9d1f3-114">**CThreadBase**</span></span>](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | <span data-ttu-id="9d1f3-115">Uma classe base que fornece os mecanismos internos de segurança de thread para o WMI Provider Framework.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-115">A base class that supplies the internal thread safety mechanisms for the WMI Provider Framework.</span></span>                                                                                                                    |
| [<span data-ttu-id="9d1f3-116">**CWbemGlueFactory**</span><span class="sxs-lookup"><span data-stu-id="9d1f3-116">**CWbemGlueFactory**</span></span>](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | <span data-ttu-id="9d1f3-117">Parte do WMI Provider Framework.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-117">Part of the WMI Provider Framework.</span></span> <span data-ttu-id="9d1f3-118">O Provider Framework implementa métodos dessa interface internamente para criar novas instâncias de classes para o provedor.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-118">The Provider Framework implements methods of this interface internally to create new instances of classes for the provider.</span></span>                                                     |
| [<span data-ttu-id="9d1f3-119">**CWbemProviderGlue**</span><span class="sxs-lookup"><span data-stu-id="9d1f3-119">**CWbemProviderGlue**</span></span>](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | <span data-ttu-id="9d1f3-120">Implementa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e métodos que controlam o carregamento e o descarregamento do provedor de estrutura.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-120">Implements [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and methods that control the loading and unloading of the framework provider.</span></span>                                                                             |
| [<span data-ttu-id="9d1f3-121">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="9d1f3-121">**Provider**</span></span>](/windows/desktop/api/Provider/nl-provider-provider)                   | <span data-ttu-id="9d1f3-122">Contém funções auxiliares e fornece implementações padrão dos métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="9d1f3-122">Contains helper functions and provides default implementations of the methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>                                                                                            |



 

<span data-ttu-id="9d1f3-123">Observe que muitos dos métodos de estrutura usam [**parâmetros CHString.**](chstring.md)</span><span class="sxs-lookup"><span data-stu-id="9d1f3-123">Note that many of the framework methods use [**CHString**](chstring.md) parameters.</span></span> <span data-ttu-id="9d1f3-124">**CHString dá** suporte a muitos dos mesmos métodos e propriedades que o MFC (MFC), mas sem a sobrecarga do MFC.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-124">**CHString** supports many of the same methods and properties as the Microsoft Foundation Classes (MFC), but without the overhead of MFC.</span></span> <span data-ttu-id="9d1f3-125">Para obter mais informações sobre **CHString,** consulte **Referência de classe CHString**.</span><span class="sxs-lookup"><span data-stu-id="9d1f3-125">For more information about **CHString**, see **CHString Class Reference**.</span></span>

 

 
