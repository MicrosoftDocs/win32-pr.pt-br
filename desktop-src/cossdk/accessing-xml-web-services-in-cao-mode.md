---
description: Se o serviço Web XML que você deseja acessar foi criado pela exposição de um aplicativo COM+, considere acessá-lo no modo de objeto ativado pelo cliente (CAO), que evita a geração de um proxy e aumenta o desempenho usando conexões persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Acessando serviços Web XML no modo CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810493"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="5eb03-103">Acessando serviços Web XML no modo CAO</span><span class="sxs-lookup"><span data-stu-id="5eb03-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="5eb03-104">Se o serviço Web XML que você deseja acessar foi criado pela exposição de um aplicativo COM+, considere acessá-lo no modo de objeto ativado pelo cliente (CAO), que evita a geração de um proxy e aumenta o desempenho usando conexões persistentes.</span><span class="sxs-lookup"><span data-stu-id="5eb03-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="5eb03-105">Para acessar um serviço Web XML no modo CAO, primeiro [exporte](exporting-a-soap-enabled-application.md) o aplicativo habilitado para SOAP correspondente do servidor no modo proxy e, em seguida, [importe](importing-a-soap-enabled-application.md) o aplicativo para o cliente do qual você deseja acessar o aplicativo como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="5eb03-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="5eb03-106">Os componentes do aplicativo podem então ser instanciados no cliente, assim como os componentes de aplicativos locais, por exemplo, usando **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="5eb03-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="5eb03-107">Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="5eb03-107">User Interface</span></span>

<span data-ttu-id="5eb03-108">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="5eb03-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="5eb03-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5eb03-109">Visual Basic</span></span>

<span data-ttu-id="5eb03-110">O fragmento de código Visual Basic a seguir ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML no modo CAO.</span><span class="sxs-lookup"><span data-stu-id="5eb03-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="5eb03-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="5eb03-111">C/C++</span></span>

<span data-ttu-id="5eb03-112">O fragmento de código a seguir ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML no modo CAO.</span><span class="sxs-lookup"><span data-stu-id="5eb03-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="5eb03-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5eb03-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb03-114">Acessando serviços Web XML no modo WKO</span><span class="sxs-lookup"><span data-stu-id="5eb03-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="5eb03-115">Visão geral do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="5eb03-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="5eb03-116">Criando Serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="5eb03-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="5eb03-117">Protegendo serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="5eb03-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 
