---
description: Você pode acessar e usar qualquer serviço Web XML, mesmo que esse serviço Web XML não tenha sido criado usando COM+ ou mesmo Microsoft Windows, desde que o serviço Web XML publique uma descrição WSDL de sua sintaxe.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Acessando serviços Web XML no modo WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646323"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="06c10-103">Acessando serviços Web XML no modo WKO</span><span class="sxs-lookup"><span data-stu-id="06c10-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="06c10-104">Você pode acessar e usar qualquer serviço Web XML, mesmo que esse serviço Web XML não tenha sido criado usando COM+ ou mesmo Microsoft Windows, desde que o serviço Web XML publique uma descrição WSDL de sua sintaxe.</span><span class="sxs-lookup"><span data-stu-id="06c10-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="06c10-105">Basta criar uma instância do componente usando o moniker SOAP: WSDL = URL, em que URL é a URL da descrição WSDL do serviço Web XML que você deseja acessar.</span><span class="sxs-lookup"><span data-stu-id="06c10-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="06c10-106">Esse é o modo WKO (well-known Object) de acessar Web Services XML.</span><span class="sxs-lookup"><span data-stu-id="06c10-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="06c10-107">Os métodos do objeto podem ser chamados sem considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="06c10-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="06c10-108">O serviço Web XML é acessado por meio de uma consulta SOAP e a resposta é interpretada de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="06c10-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="06c10-109">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="06c10-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="06c10-110">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="06c10-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="06c10-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="06c10-111">Visual Basic</span></span>

<span data-ttu-id="06c10-112">O fragmento de código do Microsoft Visual Basic a seguir ilustra o uso de um serviço Web XML no modo WKO.</span><span class="sxs-lookup"><span data-stu-id="06c10-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="06c10-113">Neste fragmento de código, que ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML, servername é o nome de domínio totalmente qualificado do servidor que oferece o Web Service XML; vroot é o diretório raiz virtual do IIS do qual o serviço Web XML é exposto; e progID é o ProgID do componente que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="06c10-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="06c10-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="06c10-114">C/C++</span></span>

<span data-ttu-id="06c10-115">O fragmento de código a seguir ilustra o uso de um serviço Web XML no modo WKO.</span><span class="sxs-lookup"><span data-stu-id="06c10-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="06c10-116">Neste fragmento de código, que ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML, servername é o nome de domínio totalmente qualificado do servidor que oferece o Web Service XML; vroot é o diretório raiz virtual do IIS do qual o serviço Web XML é exposto; e progID é o ProgID do componente que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="06c10-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c10-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="06c10-117">Remarks</span></span>

<span data-ttu-id="06c10-118">Quando um serviço Web XML é acessado pela primeira vez no modo WKO, o COM+ gera um cliente proxy e o compila em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="06c10-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="06c10-119">Essa geração de tempo de execução e a falta de conexões persistentes no modo WKO resulta em um desempenho significativamente reduzido em comparação com o modo CAO.</span><span class="sxs-lookup"><span data-stu-id="06c10-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06c10-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06c10-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c10-121">Acessando serviços Web XML no modo CAO</span><span class="sxs-lookup"><span data-stu-id="06c10-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="06c10-122">Visão geral do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="06c10-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="06c10-123">Criando Serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="06c10-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="06c10-124">Protegendo serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="06c10-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



