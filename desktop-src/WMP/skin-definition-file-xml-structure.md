---
title: Estrutura XML do arquivo de definição de aparência
description: Estrutura XML do arquivo de definição de aparência
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- Criando capas, arquivos de definição de capa
- Capas do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, estrutura XML
- Estrutura XML para arquivos de definição de capa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005784"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="db5f2-109">Estrutura XML do arquivo de definição de aparência</span><span class="sxs-lookup"><span data-stu-id="db5f2-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="db5f2-110">O arquivo de definição de capa é escrito em XML.</span><span class="sxs-lookup"><span data-stu-id="db5f2-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="db5f2-111">Um dos recursos importantes do XML é que ele é totalmente estruturado e é semelhante a uma estrutura de tópicos.</span><span class="sxs-lookup"><span data-stu-id="db5f2-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="db5f2-112">O código XML é simplesmente uma série de elementos, como **View** e **Button**.</span><span class="sxs-lookup"><span data-stu-id="db5f2-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="db5f2-113">Você começará com os elementos e, em seguida, os definirá com atributos.</span><span class="sxs-lookup"><span data-stu-id="db5f2-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="db5f2-114">O restante deste tutorial fornecerá detalhes sobre os atributos, mas aqui está o contorno dos elementos que serão usados:</span><span class="sxs-lookup"><span data-stu-id="db5f2-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="db5f2-115">Tendo em mente a estrutura simples dos elementos, você pode fazer sentido dos atributos que tornam cada elemento exclusivo.</span><span class="sxs-lookup"><span data-stu-id="db5f2-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="db5f2-116">Os detalhes de cada elemento serão abordados nos tópicos restantes desta seção.</span><span class="sxs-lookup"><span data-stu-id="db5f2-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="db5f2-117">Para obter mais informações sobre elementos e atributos, consulte a [referência de programação de capa](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="db5f2-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db5f2-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db5f2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db5f2-119">**Criando o arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="db5f2-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




