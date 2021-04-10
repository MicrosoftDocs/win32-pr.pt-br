---
title: Usando o System-Supplied substituto
description: Usando o System-Supplied substituto
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292809"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="4f0dd-103">Usando o System-Supplied substituto</span><span class="sxs-lookup"><span data-stu-id="4f0dd-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="4f0dd-104">Para usar o substituto fornecido pelo sistema para o servidor DLL, registre a DLL especificando uma cadeia de caracteres vazia ou **nula** para o valor [DllSurrogate](dllsurrogate.md) no registro.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="4f0dd-105">Quando uma solicitação de ativação para um servidor DLL é criada para o COM, o COM inicia o processo substituto padrão e a DLL solicitada (especificando o CLSID na linha de comando de inicialização internamente) ao mesmo tempo para evitar uma chamada separada.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="4f0dd-106">(Para obter informações sobre como executar mais de um servidor DLL em um processo substituto, consulte [compartilhamento substituto](surrogate-sharing.md).)</span><span class="sxs-lookup"><span data-stu-id="4f0dd-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="4f0dd-107">A implementação padrão do processo substituto é um servidor pseudo COM o estilo de modelo de Threading misto.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="4f0dd-108">Quando vários servidores DLL são carregados em um único processo substituto, esse processo garante que cada servidor DLL seja instanciado usando o modelo de threading especificado no registro para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="4f0dd-109">Todos os servidores de thread livre carregados residirão juntos no apartamento multi-threaded, enquanto cada servidor Apartment-Threading residirá em um apartamento de thread único.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="4f0dd-110">Se um servidor DLL oferecer suporte a ambos os modelos de Threading, o COM escolherá multithreading.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="4f0dd-111">Esse processo substituto é escrito de forma que o COM manipule o descarregamento de servidores DLL e o encerramento do processo substituto.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="4f0dd-112">O substituto fornecido pelo sistema funcionará muito bem para a maioria dos desenvolvedores, bem como muito fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="4f0dd-113">No entanto, esses desenvolvedores com considerações especiais podem decidir que um substituto personalizado é necessário.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="4f0dd-114">Para obter mais informações, consulte [escrevendo um substituto personalizado](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="4f0dd-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f0dd-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f0dd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f0dd-116">Substitutos de DLL</span><span class="sxs-lookup"><span data-stu-id="4f0dd-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




