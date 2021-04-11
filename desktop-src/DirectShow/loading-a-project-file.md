---
description: Carregando um arquivo de projeto
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Carregando um arquivo de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163778"
---
# <a name="loading-a-project-file"></a><span data-ttu-id="296f6-103">Carregando um arquivo de projeto</span><span class="sxs-lookup"><span data-stu-id="296f6-103">Loading a Project File</span></span>

<span data-ttu-id="296f6-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="296f6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="296f6-105">Para carregar um arquivo de projeto, você precisa de dois componentes: o analisador XML e uma linha do tempo vazia.</span><span class="sxs-lookup"><span data-stu-id="296f6-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="296f6-106">O analisador XML lê um arquivo de projeto XML e cria cada objeto definido no arquivo.</span><span class="sxs-lookup"><span data-stu-id="296f6-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="296f6-107">Em seguida, ele insere os objetos na linha do tempo e define os atributos da linha do tempo, como a taxa de quadros padrão.</span><span class="sxs-lookup"><span data-stu-id="296f6-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="296f6-108">O exemplo de código a seguir carrega um arquivo.</span><span class="sxs-lookup"><span data-stu-id="296f6-108">The following code example loads a file.</span></span>


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



<span data-ttu-id="296f6-109">O analisador expõe a interface [**IXml2Dex**](ixml2dex.md) , que contém métodos para carregar e salvar arquivos de projeto.</span><span class="sxs-lookup"><span data-stu-id="296f6-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="296f6-110">A linha do tempo expõe a interface [**IAMTimeline**](iamtimeline.md) , que contém métodos para manipular a linha do tempo e criar novos objetos de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="296f6-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="296f6-111">Chame a função **CoCreateInstance** para criar cada componente, conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="296f6-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="296f6-112">Lembre-se de que, ao criar uma nova instância, você está incrementando a contagem de referência na interface.</span><span class="sxs-lookup"><span data-stu-id="296f6-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="296f6-113">Para evitar vazamentos de memória, sempre libere uma interface quando você estiver usando-a.</span><span class="sxs-lookup"><span data-stu-id="296f6-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="296f6-114">Neste exemplo, o ponteiro para **IXml2Dex** não é necessário para mais nada, para que você possa liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="296f6-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="296f6-115">O ponteiro para **IAMTimeline** ainda é necessário para visualizar a linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="296f6-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="296f6-116">O método [**IXml2Dex:: readxmlfile**](ixml2dex-readxmlfile.md) lê o arquivo especificado e popula a linha do tempo com os objetos definidos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="296f6-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="296f6-117">O nome do arquivo é especificado usando um valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="296f6-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="296f6-118">Para encurtar o exemplo, o nome do arquivo no exemplo é fornecido como uma cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="296f6-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="296f6-119">Normalmente, você o obtém de uma caixa de diálogo de arquivo aberto ou algo semelhante.</span><span class="sxs-lookup"><span data-stu-id="296f6-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="296f6-120">Se o método **ReadXml** for bem-sucedido, ele retornará um código de êxito.</span><span class="sxs-lookup"><span data-stu-id="296f6-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="296f6-121">Caso contrário, ele retornará um código de erro como VFW \_ E \_ formato de \_ arquivo inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="296f6-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="296f6-122">Sempre verifique o valor de retorno para tratar as condições de erro normalmente.</span><span class="sxs-lookup"><span data-stu-id="296f6-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="296f6-123">Novamente, para resumir, o código de exemplo não verifica se há erros.</span><span class="sxs-lookup"><span data-stu-id="296f6-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="296f6-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="296f6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="296f6-125">Carregando e visualizando um projeto</span><span class="sxs-lookup"><span data-stu-id="296f6-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



