---
description: 'Os métodos IWbemServices:: ExecMethod ou ExecMethodAsync exigem a \_ \_ classe de sistema Parameters como um contêiner em pInParams se o método que eles estão executando tiver argumentos de entrada.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Criando objetos de parâmetros em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165336"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="06063-103">Criando objetos de parâmetros em C++</span><span class="sxs-lookup"><span data-stu-id="06063-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="06063-104">Os métodos [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) exigem a classe de sistema [**\_ \_ Parameters**](--parameters.md) como um contêiner em *pInParams* se o método que eles estão executando tiver argumentos de entrada.</span><span class="sxs-lookup"><span data-stu-id="06063-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="06063-105">O procedimento a seguir descreve como criar uma instância da classe de sistema [**\_ \_ Parameters**](--parameters.md) para armazenar informações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="06063-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="06063-106">**Para criar uma instância de \_ \_ parâmetros**</span><span class="sxs-lookup"><span data-stu-id="06063-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="06063-107">Determine o caminho de classe da classe que contém a definição do método.</span><span class="sxs-lookup"><span data-stu-id="06063-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="06063-108">Usando o caminho de classe e o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) passado de [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), chame [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar as classes de parâmetro de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="06063-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="06063-109">O método [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retorna um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para acessar cada uma dessas classes.</span><span class="sxs-lookup"><span data-stu-id="06063-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="06063-110">Usando o ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para a classe de saída, chame [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) para criar uma instância da classe.</span><span class="sxs-lookup"><span data-stu-id="06063-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="06063-111">Preencha a instância de classe definindo as propriedades que correspondem aos valores de saída e, se houver um valor de retorno para o método, a propriedade [ReturnValue](creating-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="06063-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="06063-112">Passe a instância de [**\_ \_ parâmetros**](--parameters.md) de volta para o chamador por meio do método [**IWbemObjectSink:: indicativo**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="06063-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="06063-113">Depois que um provedor de método determina que os parâmetros de entrada estão corretos, o método apontado por *strMethodName* pode ainda passar ou falhar.</span><span class="sxs-lookup"><span data-stu-id="06063-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="06063-114">Alguns provedores de método geram um segundo thread para implementar o método para que o êxito ou a falha real do método acabe sendo relatado para o chamador por meio de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="06063-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="06063-115">Observe que **IWbemObjectSink:: SetStatus** não recebe o código de retorno do método do provedor.</span><span class="sxs-lookup"><span data-stu-id="06063-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="06063-116">No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se falhou por motivos mecânicos.</span><span class="sxs-lookup"><span data-stu-id="06063-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06063-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06063-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06063-118">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="06063-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="06063-119">**IWbemCallResult:: getresultobject**</span><span class="sxs-lookup"><span data-stu-id="06063-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="06063-120">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="06063-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="06063-121">**IWbemServices:: ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="06063-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



