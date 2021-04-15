---
title: Transferência de dados
description: Transferência de dados
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498803"
---
# <a name="data-transfer"></a><span data-ttu-id="8daec-103">Transferência de dados</span><span class="sxs-lookup"><span data-stu-id="8daec-103">Data Transfer</span></span>

<span data-ttu-id="8daec-104">O COM (Component Object Model) fornece um mecanismo padrão para transferir dados entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8daec-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="8daec-105">Esse mecanismo é o *objeto de dados*, que é simplesmente qualquer objeto com que implementa a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="8daec-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="8daec-106">Alguns objetos de dados, como uma parte do texto copiado para a área de transferência, têm **IDataObject** como sua única interface.</span><span class="sxs-lookup"><span data-stu-id="8daec-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="8daec-107">Outros, como objetos de documento compostos, expõem várias interfaces, das quais **IDataObject** é simplesmente um.</span><span class="sxs-lookup"><span data-stu-id="8daec-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="8daec-108">Os objetos de dados são fundamentais para o trabalho de documentos compostos, embora também tenham um aplicativo generalizado fora dessa tecnologia OLE.</span><span class="sxs-lookup"><span data-stu-id="8daec-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="8daec-109">Ao trocar ponteiros para um objeto de dados, os provedores e consumidores de dados podem gerenciar transferências de dados de maneira uniforme, independentemente do formato dos dados, do tipo de mídia usado para transferir os dados ou do dispositivo de destino no qual ele deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="8daec-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="8daec-110">Você pode incluir o suporte em seu aplicativo para transferências de área de transferência básica, arrastar e soltar transferências e transferências de documentos compostos OLE com uma única implementação de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="8daec-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="8daec-111">Tendo feito isso, a quantidade de código necessária para acomodar a semântica especial de cada protocolo é mínima.</span><span class="sxs-lookup"><span data-stu-id="8daec-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="8daec-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="8daec-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8daec-113">Interfaces Transferência de Dados</span><span class="sxs-lookup"><span data-stu-id="8daec-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="8daec-114">Formatos de dados e mídia de transferência</span><span class="sxs-lookup"><span data-stu-id="8daec-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="8daec-115">Arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="8daec-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="8daec-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8daec-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8daec-117">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="8daec-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




