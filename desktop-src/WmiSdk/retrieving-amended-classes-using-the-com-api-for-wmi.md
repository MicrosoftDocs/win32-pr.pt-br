---
description: 'Se você estiver usando a API COM para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade no parâmetro strLocale para a interface IWbemLocator:: ConnectServer.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recuperando classes corrigidas usando a API COM para o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663242"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a><span data-ttu-id="dbe37-103">Recuperando classes corrigidas usando a API COM para o WMI</span><span class="sxs-lookup"><span data-stu-id="dbe37-103">Retrieving Amended Classes Using the COM API for WMI</span></span>

<span data-ttu-id="dbe37-104">Se você estiver usando a API COM para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade no parâmetro *strLocale* para a interface [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="dbe37-104">If you are using the COM API for WMI to retrieve or store localized class information, specify the locale in the *strLocale* parameter to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface.</span></span> <span data-ttu-id="dbe37-105">Ao ler ou gravar classes corrigidas, indique que você deseja usar definições de classe localizadas \_ especificando \_ o sinalizador WBEM use \_ \_ qualificadores corrigidos como um sinalizador para o parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="dbe37-105">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS as a flag for the *iFlags* parameter.</span></span>

<span data-ttu-id="dbe37-106">A tabela a seguir lista as versões síncronas e assíncronas dos métodos que usam o sinalizador WBEM \_ \_ usar \_ sinalizador de \_ qualificadores corrigidos.</span><span class="sxs-lookup"><span data-stu-id="dbe37-106">The following table lists the synchronous and asynchronous versions of the methods that use the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span>



| <span data-ttu-id="dbe37-107">Método síncrono</span><span class="sxs-lookup"><span data-stu-id="dbe37-107">Synchronous Method</span></span>                                                            | <span data-ttu-id="dbe37-108">Método assíncrono</span><span class="sxs-lookup"><span data-stu-id="dbe37-108">Asynchronous Method</span></span>                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbe37-109">**IWbemServices:: CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="dbe37-109">**IWbemServices::CreateClassEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [<span data-ttu-id="dbe37-110">**IWbemServices:: CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="dbe37-110">**IWbemServices::CreateClassEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [<span data-ttu-id="dbe37-111">**IWbemServices:: CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="dbe37-111">**IWbemServices::CreateInstanceEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [<span data-ttu-id="dbe37-112">**IWbemServices:: CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="dbe37-112">**IWbemServices::CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [<span data-ttu-id="dbe37-113">**IWbemServices:: ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="dbe37-113">**IWbemServices::ExecQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [<span data-ttu-id="dbe37-114">**IWbemServices:: ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="dbe37-114">**IWbemServices::ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [<span data-ttu-id="dbe37-115">**IWbemServices:: GetObject**</span><span class="sxs-lookup"><span data-stu-id="dbe37-115">**IWbemServices::GetObject**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [<span data-ttu-id="dbe37-116">**IWbemServices:: GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="dbe37-116">**IWbemServices::GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [<span data-ttu-id="dbe37-117">**IWbemServices::P utClass**</span><span class="sxs-lookup"><span data-stu-id="dbe37-117">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [<span data-ttu-id="dbe37-118">**IWbemServices::P utClassAsync**</span><span class="sxs-lookup"><span data-stu-id="dbe37-118">**IWbemServices::PutClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [<span data-ttu-id="dbe37-119">**IWbemServices::P utInstance**</span><span class="sxs-lookup"><span data-stu-id="dbe37-119">**IWbemServices::PutInstance**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [<span data-ttu-id="dbe37-120">**IWbemServices::P utInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="dbe37-120">**IWbemServices::PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



